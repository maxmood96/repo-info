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
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:f885e7f548ca1f4c6bd222b93d59234fb3ce76eb8300471493b4a63fc8a29697
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
$ docker pull irssi@sha256:b4faa0edd6642dfdc1fffc464a7d559e5192eb1bca9146bc9764db882b30a850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51084477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13e2c3737fd025087655401a2502ce4ca39d09625939260f2263defbe788241`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a22e0e8adae80ba85185210b6d8e63da9877dd0b1fda5ad24701757d84aaaa5`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.3 MB (18268872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9394069441e24f3dc53e0e015158984013db6d3871759f99a479fcbd2c576d9`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bddf1ebdebe14a1247bfa56192746485b5d33898085ef9d9d3c6d42d2007c`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 4.6 MB (4592944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:872548ddba4b2e9fe174e0b8ece2531bdffdfe772d1876e16d6d07ba1fced919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57ee2689561490c861fb9c1dceafd4ff6eaa5a7e422a229dc73d9b363da0374`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa67b764d1cad4af28c32eae921ff7b4d7d950541929bd00bdbf92f5cf7bdf`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 5.4 MB (5378461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fa90346d8a556801e906e778ce53db1089868fb7d200abfcc8291cc3909334`  
		Last Modified: Tue, 25 Feb 2025 02:16:38 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:86d2ba33abddb47801c418a8f2218b311664dd7b2d6179d63ef17a971b0eb813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47228390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bda22e0cf01282007546889f6bbe94bd4b43d9f688225e0ef79c8ab6f27394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45781f6a66f0a9873fe8fc981a82736059a119f51fabf13a7fca2408dc6fc356`  
		Last Modified: Tue, 25 Feb 2025 02:31:57 GMT  
		Size: 17.0 MB (17039825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675c4856184c664e9ad37ae69e05431783a1c96c937a821f3060c06f9279b33`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a996933ad9e9fc83330868d42a5302ff357a499011aca8df319b34ee2a33039`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 4.4 MB (4444576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c315bd4c6b3a1e32b71c51b97d9d3350029ec0e52374eca29c6ae8e3f75701bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fafeccbc9127b7ce578e8db8f026e39ff8b7431aec33a7906bfeb45fdfd4e99`

```dockerfile
```

-	Layers:
	-	`sha256:1b14fc017b1f59bda796bf9db4947b6df567055bc0b9ec9161a869846ed77d6e`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 5.4 MB (5380070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a051c05161f767cfd1f092702d2ed58b097939895529b1a05eae6e5f87b96392`  
		Last Modified: Tue, 25 Feb 2025 02:31:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4f07a8ae5110a9eb7f94cfaa96e9e570006d1c2d70b2354f735f40a6c201db4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44856983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91651364e74a63f2ca6facf5126b283198e7be3f3a783c763d30d502fbee65b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd7ba17f89be984200a57c0409fb57334d19a8199164a7e15d8de8cb786accc`  
		Last Modified: Tue, 25 Feb 2025 02:30:51 GMT  
		Size: 16.6 MB (16634749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc0ba87719f79035ec730c8b46db8e533e5fefffad050c46b0f90f788b8249d`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391be3951a8951b1d3d1ab0cae16603c155899ca274b367ce1470bb48ebe3fd5`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 4.3 MB (4299141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:aa43fb005da66915d97a391effb9ad0cde807992290eab14cd0586d77a9bb888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a3a26fb339bc257cadf6a63915bbb927d4c18c8df6ec3b28f7401821bc09f`

```dockerfile
```

-	Layers:
	-	`sha256:09144804c55584f38d877e3b74e966a298ac17eaa86df58a7be7507f99284744`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 5.4 MB (5379819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e05b7c384992d69e816cbd0928967d97e2a2250d1491ca0ce2ccbfa4c9a3f09`  
		Last Modified: Tue, 25 Feb 2025 02:30:50 GMT  
		Size: 18.8 KB (18847 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:49e93504c2f561cc24359e2823084ee2b2e1bd924dfb146ec3307127e8710c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50613635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9cc9a1a4092acb13fba1dce008e523e347e4ef44d831bc7f358b7a735f117cf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c403aa826fe5824ab781165e88b21df06dfb840cb0c804dd9cae38db1e9963`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 18.0 MB (18048732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee993cdb0b1467a98f0ed959fbfab475dd86a01d5e159eb82436546912851579`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91250615dc2027d42cc8e465b9275732ade4f0125fb67f4631314a2b77aadb10`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 4.5 MB (4513121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:daaa1ea21ea81d2192b6eac904f5d216b133be6a6b8bbc06ee343063e569454e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e9d88f6a6ddeb9553c1d22d2870ce2a340ecb8455f0c693e1a38ac612c7ff9`

```dockerfile
```

-	Layers:
	-	`sha256:4821c6d8d66791a72b3bf6fb428d61fea3af958b00af2de3e72c62b38c473e6f`  
		Last Modified: Tue, 25 Feb 2025 02:51:48 GMT  
		Size: 5.4 MB (5384937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d84f73127ab86c99bfb401ec9665c142c221dccb1694813658b3394a30e213`  
		Last Modified: Tue, 25 Feb 2025 02:51:47 GMT  
		Size: 18.9 KB (18896 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:a3b1ee1e5065bd3e527edafdd76b3ffb6e54bbd333fcac5bd4ec1e0292f016f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51611930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af50d4cecd984b8049bda8eaf1a312a12ceaa066679e6cef23b3009b7a2004e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6762bf4269fbdc6653c99d29cd04c7184f4252e176c02ec6af431533ddae30`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 17.8 MB (17807313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6ec7a5632202552aef13f879cbacd2ae29398f9c9af25875051ec2ac72bbf9`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea1f1817123e93bf3b92558c26f35f0f46917b24f667740b5c99784dfe857a`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 4.6 MB (4606668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:bdda16a102ed23377b6be5f42994551bc1351530ed997d353c7fd75e2464a953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502621496ad9242cc7106a2d8757b4b3f2cca4192465b3c9c4a803e426a00b53`

```dockerfile
```

-	Layers:
	-	`sha256:0e4076f3992376f1d4bd19d3c84a6866df69dabe28f642ea8bda0e3b52e0a748`  
		Last Modified: Tue, 25 Feb 2025 02:12:42 GMT  
		Size: 5.4 MB (5374540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe296aaa5a2eb5506e8ca74dc8e419457716018312568f62e603462b1d3de065`  
		Last Modified: Tue, 25 Feb 2025 02:12:41 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:94425ef1439d598eb33e974402ec87f08d4b5bd7faa09b4e5707cd3a2279b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50002120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bae58bf6cb7f2bf0017c837ceb065af1529bbe938d002ca46e559f2a8983e5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9512fd8d04d57886f4bf7422464252f9166b64bdfc98aa2d6e3d373fa9eb968a`  
		Last Modified: Tue, 25 Feb 2025 03:08:25 GMT  
		Size: 17.0 MB (16950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e163311e4f6335e0f4e13e639595941f934a7a56e7384ca7618b8b3b918410`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e432ad133bb500753097f2e1a6574cb27a132fbf652c4dffbf419ecbc8c67`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 4.6 MB (4554891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ca246799a71835c5dd513adc1d201444f987c8ee3437385b0156cf722a5948e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffeea112a3cab5781399b5d2bf7da16381f9b3ded7e51c11070960e923f7ef5a`

```dockerfile
```

-	Layers:
	-	`sha256:33515453ecf6fe61b68e9b1c72e2ea583148a77e3e884e35012e4a37945d7623`  
		Last Modified: Tue, 25 Feb 2025 03:08:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:a001673d7a256fabda74224597482c4b3aba17d2a97cec2a2e250082032f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55662263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814331ac38d298237066d4ffbe9e14f37073a3305e4b1c976d0f32106f6bca02`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ad0ac96d4c329c15d59251f32d4e1422ad4ddbc8d2287035e408ca21d3572e`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 18.8 MB (18777774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88a64b1406caa1005ac167ccf7da3a2b6a77cef3d483cf8d19339c6922abcc`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475ffcb09d8b27ec7257a722d17f832f7bd831fa45511757688acd598e7580d7`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 4.8 MB (4828814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6c979c773c7062ccfcaeeb16ce6357f48f96a2965df3aae7aa50879caf7c3cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127f939f90271c7c732428853fc82c50ccfa64094a92e29a5f78562bbc166e6e`

```dockerfile
```

-	Layers:
	-	`sha256:1f83ae1d0e7eda9f2d702776d1095fa9568f38c493d1c2ea257665d4ba4ee114`  
		Last Modified: Tue, 25 Feb 2025 02:32:14 GMT  
		Size: 5.4 MB (5386155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b20414e0ac80e972702d497437c6f8ea24acc5f04cad5fccc1bf1008ca6b312`  
		Last Modified: Tue, 25 Feb 2025 02:32:13 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:21b2117be71f99c8d838024594d9ea5973a979e4ed05db743d59d4d0457f5a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49683280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a7343b0ce2ebe53413903e73a57ed3c64495be8196607e2b16e41f5106cebe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f460324136ca445a6786acb1ac513804a8281a6ad63b1f6a3e9f6c563bb83d5c`  
		Last Modified: Tue, 25 Feb 2025 02:29:55 GMT  
		Size: 18.2 MB (18228328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaacee464fad5e9f10a4c3c2b5d01e4f25f28a22726d6da9e7d31551b1690af`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec9dd6db8204690ebaa62c23b128fd0e115036e43d47b4686f8eaabf657eb32`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 4.6 MB (4586753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c255e6bd75fcc5a7efb1e3c20128e0e1702364bb7f009fa5ccd9bfd250179e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa4cb39a657676cb1b444cfa04881ca30241e7431e34ca1ccfc7f588ed579df`

```dockerfile
```

-	Layers:
	-	`sha256:85ee6382fdb2c3e3b840f50077ad1d840c5c37a2e6fb5d012c7b3e52f5808a71`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 5.4 MB (5377655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe2a151d9bc2b789c2a4446d883dd46a9a8ec2ebcd1c92e0dd42a65a3360a04`  
		Last Modified: Tue, 25 Feb 2025 02:29:54 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json
