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
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.23`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.23`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.23`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.23`

```console
$ docker pull irssi@sha256:6647a2a848170ea871a21ea733940256316481652ad572817e01d1db156292dc
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
$ docker pull irssi@sha256:bb3889b9979d116f93e8f106694d0adffdd21f9af382d059ffed01c0996cc74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20782294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dc167667bffb65df976553729c71657be722d125b538e0066a708a2146db29`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:20 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:28:20 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:28:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:28:20 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:33 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:33 GMT
USER user
# Thu, 18 Dec 2025 00:28:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24415cb187a1659ec2c53535572a43ff8bed625c84d03980a338db62b53c5da8`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 10.9 MB (10858009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dbf8cf734264e190860eadd60eb62687ae5f2501206ced06b2b33a494b4bdc`  
		Last Modified: Thu, 18 Dec 2025 00:28:41 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac3569ec7b27fbca06e7b4db52a312f39068102b286cb92119735bbe34ef52`  
		Last Modified: Thu, 18 Dec 2025 00:28:45 GMT  
		Size: 6.1 MB (6063195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:073bb57393cdce4cd0d1e1528352c45270b1ae708b6dca9069f5be81956397b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff68a5f7c6693cfe00a22c0d6f8667c0a1a525eb02cf4dcc96c366d8e79474`

```dockerfile
```

-	Layers:
	-	`sha256:40bebfa7651a8632ee17f45a3df6d936aa0fadd11dd0534e567ac9bd6daee4a9`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 1.3 MB (1308739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f8b6a61e39c5a92432c5627cc439edcc016195f6ff883f4fb598e3d94a84107`  
		Last Modified: Thu, 18 Dec 2025 02:59:42 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bad9d7fcd0e28d67bab47fb90d795dcc2eaf4c4a0b2e3d90a07cee972bae66dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19537826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1149a631c9c56dcba7d2e6c5aafa93f894c93d84c6d2bf78a86e52893e31873c`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:41 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:26:41 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:26:41 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:26:41 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:26:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:26:58 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:26:58 GMT
USER user
# Thu, 18 Dec 2025 00:26:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcb7ff81309b2e31723eaf47065f1c998586d9e1452ebd80783680e18130d4a`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 10.1 MB (10075319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5403bddc0bbc9930be28ad858bfa3b7906f59e970c1370d9fc6a83f44e6fbe2`  
		Last Modified: Thu, 18 Dec 2025 00:27:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1ad234a7984764ff6f457100bb9b1d34907fe5464fb1ebb2517f7361ded63`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 5.9 MB (5893091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:0e8e5d93d188728ba16ed8406cab8e289e1c2a1ee1594922b7556d9f74abe879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811618f7deae2dd8332c12cd7a8984ed3dd6097d93c210d5c427e49563e5b4dc`

```dockerfile
```

-	Layers:
	-	`sha256:fd32f6a87a34210ca3faf3b8fe174b80277423c9c6a6df9c3715397d452e912e`  
		Last Modified: Thu, 18 Dec 2025 00:27:04 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:5545fe384592a03b386ec71c34d9628fb7219e0cea85e058644cc6f2554698ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18825958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d396de0839b37b889c56a300cb5cd42732bbd07a7983c50428250cd1bb906b84`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:27:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:27:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:27:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:28:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:28:03 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:28:03 GMT
USER user
# Thu, 18 Dec 2025 00:28:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0adf1406272cc1c92a0fb79705a64b63974803df9a03ac3834f310852b5b36`  
		Last Modified: Thu, 18 Dec 2025 00:28:19 GMT  
		Size: 9.9 MB (9902369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e16179b1f560e9b9950ef37b539610d827769f23a101b0c7e740a0269a713`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1636b9f7c0a2d3ad3183282573bd9f5e57dd5c4736c4bb32382a7709f8a01f`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 5.6 MB (5643216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f00b846b1722b6d761ae64d9494a2ee11a253e67da578d70ca3b3b3b15520100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1328781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d7aba625cc57b97c787ef76eaf4dc8a3d3af88eddf3d0ee4ede652b9fbea3`

```dockerfile
```

-	Layers:
	-	`sha256:99ef1e8bfb56b9655ad6b84bedcbea48574ad9ec46c1c3fd40c522b825aa504a`  
		Last Modified: Thu, 18 Dec 2025 02:59:50 GMT  
		Size: 1.3 MB (1311147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de2bfcc35f922ee69d1758db7a3f63d920670e9631558ad99d7599dd2a25e2e9`  
		Last Modified: Thu, 18 Dec 2025 00:28:11 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:55bf7e12e3b4ee093eae33b2fa1f5c96090535c9348e52568bdc97a0a293b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20925819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4b7d1238dd9a3adde6ead454a538ad8284cbf7f24894efb5672a05bbcfce0a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:22 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:23 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:23 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:35 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:35 GMT
USER user
# Thu, 18 Dec 2025 00:29:35 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7348e6f70eb616dea13b24e36898da83685b6925b47ec95e36057de2c1783047`  
		Last Modified: Thu, 18 Dec 2025 00:29:43 GMT  
		Size: 10.8 MB (10792800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fddcc2c50012cdd625ec697bc298302ceff467de08484d7a52f8bcc75cb0e5`  
		Last Modified: Thu, 18 Dec 2025 00:29:42 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c05272543b6f9c8021b992983c2f6abb5885750f05739dc1d25c4ee08c98ee`  
		Last Modified: Thu, 18 Dec 2025 00:29:49 GMT  
		Size: 5.9 MB (5936291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:029ab7e48f7e81738e87e112dd9f2a9318068bfd97cd655c8e90a924d5a12146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d27ba912daad8618487cf32866018e0740bcd76c8108bf7c7f319ae627f893`

```dockerfile
```

-	Layers:
	-	`sha256:94fd0d4f70d7c342ee96ffec8cf2011dacae14e3e75cb3bfee3758616c2ea786`  
		Last Modified: Thu, 18 Dec 2025 02:59:54 GMT  
		Size: 1.3 MB (1308193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0086b52c2f32c8d1ecbf9478f9509889c8e16b2d5833797968604527de119f7c`  
		Last Modified: Thu, 18 Dec 2025 02:59:55 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:cfdf743bb09ab2a4ba7764ad5696a737bafc95759e64bb79f6bfaf4d883e4b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20224751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30f0695a51eeaae5b208469d4b38368b224ce8aaa475d9bd1b993572f6d7c7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:30:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:30:11 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:30:11 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:30:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:30:27 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:30:27 GMT
USER user
# Thu, 18 Dec 2025 00:30:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a45b79f4fff519bbb0d6713e56628ddffcac9bc4c1543907ea2b5ecd55a3e81`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 10.4 MB (10393558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ef839ff47bbf18b73140c8712e72cb22ecca46b3e8fdd8ec68f3e34de4befc`  
		Last Modified: Thu, 18 Dec 2025 00:30:34 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98002cef64891cb9416a0c31f904ec9037b3401b618c75aa06851347032fa0b`  
		Last Modified: Thu, 18 Dec 2025 00:30:41 GMT  
		Size: 6.1 MB (6144108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:fb68f05d44e0c0db000a0af566e3426523e7f0b9f32e6d76722afa1c980fc51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829f5635556fb11f2ffd77cb7c8c5cadd983850234d620b1f52a7bccbdd5257e`

```dockerfile
```

-	Layers:
	-	`sha256:d09e7a63b5359ab9642ec33b18393bcc6a936eca24ad4130da239409506757e7`  
		Last Modified: Thu, 18 Dec 2025 02:59:58 GMT  
		Size: 1.3 MB (1308694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec901df34838627b73c149fb922297b09aefcd820347fe989f9a8dfd62569d2`  
		Last Modified: Thu, 18 Dec 2025 02:59:59 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:1edc21eef5ba523862a28e14904175809cd4922191275610b7fd8aa9886d6b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21270362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d0df36317c631c450fdc8429b8e7e1573d928329ca7b6d649f40869fd3b248`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:32:49 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:32:49 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:32:49 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:32:49 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:33:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:33:06 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:33:06 GMT
USER user
# Thu, 18 Dec 2025 00:33:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05ca9f60e817feeab18e4a7498e423c6b8d3b05ddad6f20b6398b97464d6851`  
		Last Modified: Thu, 18 Dec 2025 00:33:26 GMT  
		Size: 11.1 MB (11079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0773f78b082a8e04dbd070d88855d25f7b33385e48784269c96d0955236a07`  
		Last Modified: Thu, 18 Dec 2025 00:33:25 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849b934c90ad92f17caabf7973f6c9ba8ac2db8aaf0e622a1afa981febbba1b2`  
		Last Modified: Thu, 18 Dec 2025 00:33:27 GMT  
		Size: 6.4 MB (6362102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:663187062a6f4f31e2868d4f25912303b6bec85674a60a859b4d799d4b25e86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a16ea254af32328cd231e5b97e700e0b1e170a9913797feeffecae8fe37c90`

```dockerfile
```

-	Layers:
	-	`sha256:14f554941d20bd86cb6713ea4ade15770f1b43e4e7aca14d4660e5b1c41f6599`  
		Last Modified: Thu, 18 Dec 2025 03:00:07 GMT  
		Size: 1.3 MB (1308146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056d16a5c94fe06a4295caeba4fe3d9cf7f7078c3eb577e90b98897d2948308a`  
		Last Modified: Thu, 18 Dec 2025 03:00:08 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:504c721baf2f3dc2a827100e130977df33a59372ee0b99048b41af0a38300cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19940844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dce54188f8af4d581975fe411a7612758765a07cc6be3e0dd204862765b11cd`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 06:34:27 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 06:34:28 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 06:34:28 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 06:34:28 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 06:38:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 06:38:13 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 06:38:13 GMT
USER user
# Thu, 18 Dec 2025 06:38:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ed6b08bc69b359229ed8133382a06af2b35202ed1c3106be842c34ccccf9`  
		Last Modified: Thu, 18 Dec 2025 06:39:06 GMT  
		Size: 10.3 MB (10291811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c13ad9ab2a723780fa2b838d6703af25ba95551a879abe0a7ff89f8ffda6a`  
		Last Modified: Thu, 18 Dec 2025 06:39:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa97c3fa13c87e7c7a414de9fff3fefaa3f914e4f0275d4e2743eb87de4166e`  
		Last Modified: Thu, 18 Dec 2025 06:39:05 GMT  
		Size: 6.1 MB (6064109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:008992bb79c6b4df709e56e1cd4fbdd249599f22671bfff5e291b8a8a3217570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20ccd3955339fe30e6e3892d394d72e687d3dd885bb6fce10baa5646f896b8b7`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ec0754039e1ffe76595dc7eaa5da9b5af6464358a08d0d7609ccde0189996`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 1.3 MB (1308142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:371664449449a4dfc4b3db6fbdbbbeae1b4daca3567fccbe04dd18e795102910`  
		Last Modified: Thu, 18 Dec 2025 06:39:04 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:c756a2583d41497d86acbdeceedac763d8b78c1aa4cab2b06fb962bd32a3b037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21333480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ff7afd32ab87f90d82ea73328da75fff8d32ff11da09cfd346ca4367b01323`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV HOME=/home/user
# Thu, 18 Dec 2025 00:29:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 18 Dec 2025 00:29:34 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:34 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 18 Dec 2025 00:29:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Thu, 18 Dec 2025 00:29:59 GMT
WORKDIR /home/user
# Thu, 18 Dec 2025 00:29:59 GMT
USER user
# Thu, 18 Dec 2025 00:29:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf10e1fc24831cde3bfbceb451baaa6db0b341cca88bb942d96866a3e546c18f`  
		Last Modified: Thu, 18 Dec 2025 00:30:12 GMT  
		Size: 11.4 MB (11405160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ef5ae49ff81b109ed7711e01e27704000d2b56bde807ad614dd136f5e1ea1c`  
		Last Modified: Thu, 18 Dec 2025 00:30:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e11d8914ce1bcfb4a65b8200e74e954fb9c3185098c6ea9e4a2e8f09b7df34`  
		Last Modified: Thu, 18 Dec 2025 00:30:24 GMT  
		Size: 6.2 MB (6203024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:5f59a9171e69187914fae3b550b39d19fd226cdc7d6fdc962f2d00a45bec539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1325588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c2dcbd5e826fe84a9ae09c7fea7a4056c8f57a83748ed074c1c0bac9795569`

```dockerfile
```

-	Layers:
	-	`sha256:129578bfd267407d257178c13dfd247287802e09b2b2618a3ec04cb45eb7935b`  
		Last Modified: Thu, 18 Dec 2025 03:00:16 GMT  
		Size: 1.3 MB (1308088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b07318c4fe73a8abcb9da36bd706b483116604273b89c463e8183a645f4fb0`  
		Last Modified: Thu, 18 Dec 2025 03:00:17 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:0ca392d0ea779c59c7c82fa9f575467133d2c744589a0c795849b4221215a6e0
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
$ docker pull irssi@sha256:e0cf8f834b2f6f1163e35b72df2e98e76c898068c096b799ee98b267dd0d0573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53866130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df99052d10a4bfd3473939f107da79703518ece1caf31f399f7ff632c18af8cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:22:08 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:22:08 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:22:08 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:22:46 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:22:46 GMT
USER user
# Tue, 13 Jan 2026 01:22:46 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6182d5f23df2701e06e47e60a7b9e4e29a67340fcd08275ab88a0cbdba141c8`  
		Last Modified: Tue, 13 Jan 2026 01:23:04 GMT  
		Size: 19.2 MB (19222294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33428feed1ae71510cbd12b62d2489b9b2a7622b71ad774701cd6c2f9d182fc`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7b137c8134733c1670895817a6c962bdcbb2ad2071f1685ca1e2132226988e`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 4.9 MB (4866796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:75bf44c6cb4b1de972b1979174a4fb617852eac7805366952503140ddb03cfd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d0e70ae6c273829f86114fe201f1437ccbb46c9991bdd7b29cea3a3bcb730b`

```dockerfile
```

-	Layers:
	-	`sha256:781becbbb0c253fc6a88661fd5ff618fb1c9c2bce3255d76af45cf4abdd6e64b`  
		Last Modified: Tue, 13 Jan 2026 06:00:10 GMT  
		Size: 5.6 MB (5588475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d747bd346a03af63c4d34f1691a93e342f3c2af80f39f9d859d5f4d36c8c65`  
		Last Modified: Tue, 13 Jan 2026 06:00:12 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:daa64e5f7066c381dbb7f0d641cefa37181ed12bc30c00caa34ebd557067dd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef2216ecf83b0e1556bc49d270a33b0adf122b824724d4efdc7c78a177f7a6d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:15:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:15:19 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:15:19 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:16:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:16:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:16:13 GMT
USER user
# Tue, 13 Jan 2026 01:16:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd87a58e51a189bcac13226ee400aeb85d8542da66ffa135c18c088d69f705dd`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 18.3 MB (18288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df27954aa7a85e8b14b35e364127561c551cb47d8b83b1dbe450f12950ca7`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ff0a7f1bc138cc472f6332e75270bfbf19047e32d5067f83c68985b52350a9`  
		Last Modified: Tue, 13 Jan 2026 01:16:29 GMT  
		Size: 4.7 MB (4710030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa46e443c151916bfbe916b074c29b175fbe8d1091eb0b9ce82732904a5239d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65f440dde20d00c045a5576d1d6addd325d82496bfe178255cb7ea0d3f96ef`

```dockerfile
```

-	Layers:
	-	`sha256:41630454bda7707796a5dbc2bf239cafaa48a2d0fb059c60512aec3031897265`  
		Last Modified: Tue, 13 Jan 2026 01:16:24 GMT  
		Size: 5.6 MB (5586024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da08d2b38599fd591234c632661c99b26560fbdfe7a6ec251486f9cf238fc65`  
		Last Modified: Tue, 13 Jan 2026 03:02:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:75ac27664ba4b00e824e5635a625acf1b34d84b3140595a05952af78ace24d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48680182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1aaf8b4a0204f34991412bf25618079d950d0a9378f9e4cabe83fa3be1721`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:24:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:24:49 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:24:49 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:25:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:25:30 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:25:30 GMT
USER user
# Tue, 13 Jan 2026 01:25:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b14ff6df0e292154a11d7c4816ee009d807bb53e3ef783fb1ba4b5f484a3490`  
		Last Modified: Tue, 13 Jan 2026 01:25:41 GMT  
		Size: 17.9 MB (17909811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f475ec0e3656b50a1642f3cf8e49ac5b2aaab3bbf66dff775e99c14c0ee2e65`  
		Last Modified: Tue, 13 Jan 2026 01:25:46 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3addf3d30e038da2eb74bc388f8160f0def905d2a3156731736b6ab375436c77`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 4.6 MB (4558431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:638de1cb43a58d8f128992690156d718f81e3998139f209d168cabde965debb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6606979c314e86a6a9e7f4553299d70822dc8bd460ba48412d8894357f8755af`

```dockerfile
```

-	Layers:
	-	`sha256:42cd0a2e63e581ab0da00ad7a7059a8d002529f6f28514b3a686d2fcddc2d4ab`  
		Last Modified: Tue, 13 Jan 2026 03:02:12 GMT  
		Size: 5.6 MB (5589046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f1d4465d577375a6f846b071d236912b37806f994eda1aac13a86a28f59bc2`  
		Last Modified: Tue, 13 Jan 2026 01:25:40 GMT  
		Size: 18.8 KB (18786 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:e2385677c3f02ce1d1fce3978cc586a52187ff93e862d47f96a2c8a6f64431a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e80aaa139390d635c16e521239bb79fccb44a57c7d4e5ada1536c95c6b0c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:21:12 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:21:12 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:21:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:21:48 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:21:48 GMT
USER user
# Tue, 13 Jan 2026 01:21:48 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa9d6199ae9b6a27dcb85fe28a884764f5e3906db0c99aff782883a72860b05`  
		Last Modified: Tue, 13 Jan 2026 01:22:00 GMT  
		Size: 19.0 MB (19049890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d59276be1dc49747de671c6cdc7816e0341bcf1065387e1f55140e1554e60`  
		Last Modified: Tue, 13 Jan 2026 01:22:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e4c435cb8ba7904c2c2394c923381cf0ee01de1cec11399cad79dcb1b4804c`  
		Last Modified: Tue, 13 Jan 2026 01:22:07 GMT  
		Size: 4.8 MB (4781516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ee89e5ea04a3cc85c3c2e79b03489402a2073dc7cffca2120dca0a9f70c3f2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1924b739feb8ee1151fac42cf19da1915d69ae3d20aea59c0fe4722f6cdaa84`

```dockerfile
```

-	Layers:
	-	`sha256:70bf4febcae38238b6b6cc80dc3f1de7b0b1669c920096e739caae40ba480a1f`  
		Last Modified: Tue, 13 Jan 2026 03:02:22 GMT  
		Size: 5.6 MB (5594959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e819fad505d9bb6e75bcc0f72d98a59e6b7a2c1b3298f9acd37b77a6b6b774b`  
		Last Modified: Tue, 13 Jan 2026 03:02:23 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:39c381d9efbd2923e3baf181cd26f4c4749474a741eeed7825a37b4fc8ae8641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54903796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f2a13041dab6ec0f785b74e2db9bbebf7d16b0a976d3624f2bae522e7f20e6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:18:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:33 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:19:13 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:19:13 GMT
USER user
# Tue, 13 Jan 2026 01:19:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc3d645d0e574a06b492ac8106cb2979ac5e45fa5a2f71c4ceb26bef3dfe730`  
		Last Modified: Tue, 13 Jan 2026 01:19:28 GMT  
		Size: 18.7 MB (18743517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea68a970e3f5f1eb384f1d520092b59af11dc993e9892f5ea7a14353c210959f`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1766948bb18f9c2d590a17715ce3b831ad107517e5d8e8de67070e96467ffc`  
		Last Modified: Tue, 13 Jan 2026 01:19:27 GMT  
		Size: 4.9 MB (4868445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e4ba2215e859754353afc4f4aeaeccaec22fb8c2fae2e6bce83e57b53fb857f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4107259c1d9892c64a8d35dcafe3c96baf80023f5a83883419421d4e8408eb83`

```dockerfile
```

-	Layers:
	-	`sha256:67cf9ceeb2327fa2448099852e7fe648f7e9cc03dff382c24f934a4ca47bdc91`  
		Last Modified: Tue, 13 Jan 2026 01:19:23 GMT  
		Size: 5.6 MB (5584598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c87320071c0c5733599a24bf19a95c5cb3673c1218d8c4b1826726a7298b85af`  
		Last Modified: Tue, 13 Jan 2026 03:02:39 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:16adf43a4fbc0c781edf4ac2c2a63de44d769a5ff3a5be100ed4e9469cea9bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58239859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bafa5beea3a019c8fbeea90bf963a76ac46b771ff6d1e497a9379b969d81`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 01:27:54 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 01:27:54 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:27:54 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 01:29:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 01:29:58 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 01:29:58 GMT
USER user
# Tue, 13 Jan 2026 01:29:58 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcda9f8bbb8b1dff20f896141ba98aa8d1f215f950e6cbf45cfcd5c504ffabac`  
		Last Modified: Tue, 13 Jan 2026 01:30:28 GMT  
		Size: 19.5 MB (19542995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33da8ea705fb4e3b913ba9aa71a5679c2f6865ad7ae822867688c3b8a43cef`  
		Last Modified: Tue, 13 Jan 2026 01:30:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024d4576019b7176219803c53d4eca47bc6a6bc7c3cd2557354291db447dbdc`  
		Last Modified: Tue, 13 Jan 2026 01:30:27 GMT  
		Size: 5.1 MB (5097903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:14e74257a79657c3fe51436c56ac72551017c2eae5c54f8cb5acb5d89b26ae80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ade875137ad77b2c213390392952c0d86419b4dfdf9e55fbc8b9c1d9e2b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cd1e73aa16a569bcd34dd26fe9c066f5f5b010c6aa7b6e74f2c561f1989d9163`  
		Last Modified: Tue, 13 Jan 2026 03:02:45 GMT  
		Size: 5.6 MB (5595506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b97fa87dec42608925e73e4af2d59e591ca84ec1bf660d36f61c4465fe4edfa`  
		Last Modified: Tue, 13 Jan 2026 03:02:46 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:42f25149c195922ace2d09f52039c56d767996a84e387c8b4eb7cbce5f7c67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51685610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c351bf47836b31594adc21aa27395e93d1a031e65d60247048b80b4a4dd12c1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 06:26:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV HOME=/home/user
# Wed, 14 Jan 2026 06:26:49 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 14 Jan 2026 06:26:49 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 06:26:49 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 14 Jan 2026 06:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 14 Jan 2026 06:33:37 GMT
WORKDIR /home/user
# Wed, 14 Jan 2026 06:33:37 GMT
USER user
# Wed, 14 Jan 2026 06:33:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f9ee6f39e761595d5c9e020ae1fb10f95fe2a2951aa757f6de57a94a5d25ab`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 18.5 MB (18549843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef5f232538194de0e7b47d1c08ae77477427a3951186780b1f80e4a91600b4`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b07d932aff1dc5ee2440e07ea368a0ddb73f2c32cb1a8ab0bfd881b02a53f7`  
		Last Modified: Wed, 14 Jan 2026 06:35:42 GMT  
		Size: 4.9 MB (4860721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:0d0a172cbd5471aa3ec8392dc55c5bad0e4fe5bb8e39202b61a8ad6e7252ed2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f4f48da90e6ab7c83ee1b3d3d3112e940971d8bcbed03f47ee03a7d5cca5a6`

```dockerfile
```

-	Layers:
	-	`sha256:afd4f3e89883cc18160c077e4faf0da05c4455d6e0cf0af04a7f525621cba93f`  
		Last Modified: Wed, 14 Jan 2026 08:59:45 GMT  
		Size: 5.6 MB (5579778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d7e2d6743dc6628d707a2e9780dc009b06754202d718210a4e2690ed143c0b`  
		Last Modified: Wed, 14 Jan 2026 06:35:29 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:653361fd289685d0a3ef257222d30cb0718bc48515a9c015fbcac3f398609f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54502124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fcdf2f4ef52dfdc3c24f9428397fd9380e60fd354869f1da51fcc940955243`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV HOME=/home/user
# Tue, 13 Jan 2026 14:13:50 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 13 Jan 2026 14:13:50 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 14:13:50 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 13 Jan 2026 14:14:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 13 Jan 2026 14:14:24 GMT
WORKDIR /home/user
# Tue, 13 Jan 2026 14:14:24 GMT
USER user
# Tue, 13 Jan 2026 14:14:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9a78cbdc576318bf00aa21bf1164b61d508829b7fc88b8c23f40d95e1554`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 19.8 MB (19759529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed759cad2dcf7c6e402d05690e7dbf240c6349a4f59e7ed4dd763b7db0c7db2`  
		Last Modified: Tue, 13 Jan 2026 14:14:53 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d08518de05d2a01ab14736b1bb40de01733edd886327cf0a84c31ad058bf51`  
		Last Modified: Tue, 13 Jan 2026 14:14:54 GMT  
		Size: 4.9 MB (4905829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fb130cfa75f8d05885dcafd079c2dfbf6c712d384c0c0517fb34a7dfe94001c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bde0c93e87598e601fcf375b35b3025bcea14aa50d427eac87d0593556f33f`

```dockerfile
```

-	Layers:
	-	`sha256:f5a37598d0bc0f12bb6c93bb4c05cb053ac0b193ea89a6d7b7b4e182b3431485`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 5.6 MB (5589380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3282d1c93664386bd31d45797dbca2fab0dc0b8235241771a589dbc71a943fc4`  
		Last Modified: Tue, 13 Jan 2026 14:14:41 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
