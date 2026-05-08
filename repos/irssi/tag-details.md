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
$ docker pull irssi@sha256:fec65570aa479b8efe0378f09327819aa6e74291b73afbd2b7debb3a5253efb6
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
$ docker pull irssi@sha256:617bd6f87c82d3a3508a08c03870a148378df23d7c182b981db2d55ef51f469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2ff96bdddacb55598d36b69616332f5789463faaefdee4e891c05d394a0251`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:20:56 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:21:32 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:21:32 GMT
USER user
# Fri, 08 May 2026 19:21:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e0dfc0c55c5ed3a8ca1ee595b5a02b09796e2d03423b056378c982aabb423e`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 19.2 MB (19222370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84340c1aaeaddd3ae2c9796f3e75d1a4ce88eda4e95c7e67d15e13f5c53509ec`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e86c68f4d54621b1fc1908b3ca76d1e3f8543a639dbc504d80f5281827042b`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 4.9 MB (4866915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:fc57d3e80e06d8d240bd0e82869bea15d2b4a07d2e09855a532e9ddd8f916579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d85f0f0a3e0650fa4e58c5e5e94e4d2e094bd6c6397894e7487e5b1909be9fc`

```dockerfile
```

-	Layers:
	-	`sha256:ee08cceb270e0a961552dc474721d574add79408869c1ebf6b94e844dd997f16`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f3ff9cf829c014886ec151467a7af797ca6eb818c7bb1aa0cf3e38773a7135`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.23`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:5acc53eeb8b33947406ddc481d5fb68e9d285406df75217e27a0c4aa441ed705
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
$ docker pull irssi@sha256:88c0ccf218b4a0588bd739e0e6b36bc3627b2c2bf6ad7c878b9339310029eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a432ec7f4bc3a819553703167ea6e60f03085a1421db1308b36379f23bf407b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:20:24 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:59 GMT
USER user
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cbe811686f30430463194903c8403046a46e2cfc7863672ddaae3ea1de9ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 19.2 MB (19222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef6fc2375668881f03374a60e1e53c054a2dd9fb7d0d89d2ed20263afffacf`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066b975499f88330791f13923102ac1707a92bf511329cc8e953ac9506d06ca`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 4.9 MB (4866901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7e516331d2e35431375fec60eaa42df6ab7686f689de4d979c90297b074e8d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74664e26abe8c4bdb5efdaf62508f72ce2925a79ef9c7a6f18eedd3acd93cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b917b983fdd6d74b71df372114b8be6d79be535d12e9a231fb2de9298ea11f6`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090405506a1e903055a1c09f043bf011e58cfa6b6f9bac0d3a9a88c1343ddd4c`  
		Last Modified: Wed, 22 Apr 2026 01:21:08 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:5acc53eeb8b33947406ddc481d5fb68e9d285406df75217e27a0c4aa441ed705
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
$ docker pull irssi@sha256:88c0ccf218b4a0588bd739e0e6b36bc3627b2c2bf6ad7c878b9339310029eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a432ec7f4bc3a819553703167ea6e60f03085a1421db1308b36379f23bf407b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:20:24 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:59 GMT
USER user
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cbe811686f30430463194903c8403046a46e2cfc7863672ddaae3ea1de9ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 19.2 MB (19222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef6fc2375668881f03374a60e1e53c054a2dd9fb7d0d89d2ed20263afffacf`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066b975499f88330791f13923102ac1707a92bf511329cc8e953ac9506d06ca`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 4.9 MB (4866901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7e516331d2e35431375fec60eaa42df6ab7686f689de4d979c90297b074e8d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74664e26abe8c4bdb5efdaf62508f72ce2925a79ef9c7a6f18eedd3acd93cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b917b983fdd6d74b71df372114b8be6d79be535d12e9a231fb2de9298ea11f6`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090405506a1e903055a1c09f043bf011e58cfa6b6f9bac0d3a9a88c1343ddd4c`  
		Last Modified: Wed, 22 Apr 2026 01:21:08 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.23`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:5acc53eeb8b33947406ddc481d5fb68e9d285406df75217e27a0c4aa441ed705
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
$ docker pull irssi@sha256:88c0ccf218b4a0588bd739e0e6b36bc3627b2c2bf6ad7c878b9339310029eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a432ec7f4bc3a819553703167ea6e60f03085a1421db1308b36379f23bf407b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:20:24 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:59 GMT
USER user
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cbe811686f30430463194903c8403046a46e2cfc7863672ddaae3ea1de9ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 19.2 MB (19222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef6fc2375668881f03374a60e1e53c054a2dd9fb7d0d89d2ed20263afffacf`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066b975499f88330791f13923102ac1707a92bf511329cc8e953ac9506d06ca`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 4.9 MB (4866901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7e516331d2e35431375fec60eaa42df6ab7686f689de4d979c90297b074e8d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74664e26abe8c4bdb5efdaf62508f72ce2925a79ef9c7a6f18eedd3acd93cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b917b983fdd6d74b71df372114b8be6d79be535d12e9a231fb2de9298ea11f6`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090405506a1e903055a1c09f043bf011e58cfa6b6f9bac0d3a9a88c1343ddd4c`  
		Last Modified: Wed, 22 Apr 2026 01:21:08 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:fec65570aa479b8efe0378f09327819aa6e74291b73afbd2b7debb3a5253efb6
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
$ docker pull irssi@sha256:617bd6f87c82d3a3508a08c03870a148378df23d7c182b981db2d55ef51f469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2ff96bdddacb55598d36b69616332f5789463faaefdee4e891c05d394a0251`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:20:56 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:21:32 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:21:32 GMT
USER user
# Fri, 08 May 2026 19:21:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e0dfc0c55c5ed3a8ca1ee595b5a02b09796e2d03423b056378c982aabb423e`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 19.2 MB (19222370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84340c1aaeaddd3ae2c9796f3e75d1a4ce88eda4e95c7e67d15e13f5c53509ec`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e86c68f4d54621b1fc1908b3ca76d1e3f8543a639dbc504d80f5281827042b`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 4.9 MB (4866915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:fc57d3e80e06d8d240bd0e82869bea15d2b4a07d2e09855a532e9ddd8f916579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d85f0f0a3e0650fa4e58c5e5e94e4d2e094bd6c6397894e7487e5b1909be9fc`

```dockerfile
```

-	Layers:
	-	`sha256:ee08cceb270e0a961552dc474721d574add79408869c1ebf6b94e844dd997f16`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f3ff9cf829c014886ec151467a7af797ca6eb818c7bb1aa0cf3e38773a7135`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.23`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:fec65570aa479b8efe0378f09327819aa6e74291b73afbd2b7debb3a5253efb6
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
$ docker pull irssi@sha256:617bd6f87c82d3a3508a08c03870a148378df23d7c182b981db2d55ef51f469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2ff96bdddacb55598d36b69616332f5789463faaefdee4e891c05d394a0251`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:20:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:20:56 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:20:56 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:21:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:21:32 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:21:32 GMT
USER user
# Fri, 08 May 2026 19:21:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e0dfc0c55c5ed3a8ca1ee595b5a02b09796e2d03423b056378c982aabb423e`  
		Last Modified: Fri, 08 May 2026 19:21:43 GMT  
		Size: 19.2 MB (19222370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84340c1aaeaddd3ae2c9796f3e75d1a4ce88eda4e95c7e67d15e13f5c53509ec`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e86c68f4d54621b1fc1908b3ca76d1e3f8543a639dbc504d80f5281827042b`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 4.9 MB (4866915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:fc57d3e80e06d8d240bd0e82869bea15d2b4a07d2e09855a532e9ddd8f916579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d85f0f0a3e0650fa4e58c5e5e94e4d2e094bd6c6397894e7487e5b1909be9fc`

```dockerfile
```

-	Layers:
	-	`sha256:ee08cceb270e0a961552dc474721d574add79408869c1ebf6b94e844dd997f16`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f3ff9cf829c014886ec151467a7af797ca6eb818c7bb1aa0cf3e38773a7135`  
		Last Modified: Fri, 08 May 2026 19:21:42 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.23`

```console
$ docker pull irssi@sha256:7c2ee0882bf007852a20867f9913437ae6657fd03a331e7a77e133726ff69944
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
$ docker pull irssi@sha256:dc5df1b58e5b65a3a759880c5e85d4a3f9b00101c8714c1c641b6cc9238acaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20786977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288090f6d91eede7d4eeff9b23bc23af786c37eeadccb13bd6f3ef9437ce4336`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:42 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:42 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:42 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:42 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:54 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:54 GMT
USER user
# Wed, 15 Apr 2026 20:17:54 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c5acb2b8849dfbc3ab7dac250bb75028f186bb6733ad7177b937b31f273b8`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 10.9 MB (10858235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e7a3bff3ec07d78843e225a8924e151e5daea035461282480b5aa821e6705c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0cf822c89aa3e74cb489830e51d76afc9215694e4c95d4ff6b22e5982f04c4`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 6.1 MB (6063568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:bf8012819911dfaf56515374f681f893249b0db11ddd7bea57fa25dc0a2d09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaae6d9d2d8688519f9df33930928011c4010b1179c24d66b7d4b44adda0a44d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f70f031073a0bee5df5e94871c9c0e0c72ea88c339f9eb2a86e4dc33ac5ab9`  
		Last Modified: Wed, 15 Apr 2026 20:18:01 GMT  
		Size: 1.3 MB (1306784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c573c6f83781d7801716b88a5047725f6e4c824b5986b91bb98255f8a226a1c9`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:32a993e3ad9b91e98d7f9d895a4c4b5e2b10818f155823c0654cab147d4e8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19538989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca1094867198ce0d1a87bf43e35e11da52d537622882aff5f2c2f6b54d9b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:52 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:09 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:09 GMT
USER user
# Wed, 15 Apr 2026 20:18:09 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3b91abb913ea5e552d7b0c7347de9ef0c668c74007f3f8d596df4b3285a230`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 10.1 MB (10072770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8790e4fb41f6ece159618adf742aca7b1b3bfb4006b649fa173b52e5d9c`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bc551d614897c5e1f37a1639b18294245230dd66a0c33dc9838839592eadb`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 5.9 MB (5893373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:f8d5c8034900c66929ae9c22c2b9b1faea245ac7317a6866630af08bacf312e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d310f9907d9f56f5894b2b06bc4efc44434c529351c08426b2cb7dd2074aaab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c700ec9d42a320334d5e286c3c876a4cf0a7152772e7bdcc8d35701849b271f`  
		Last Modified: Wed, 15 Apr 2026 20:18:14 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8400cca8ce894ce77a70da43d520c1240eddff2930763ffc0372799c186d9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18831804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebe844c4e6342061059fcd093f14ed4b366024bff88c6f71a52dfeb7965d7a2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:17:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:18:08 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:18:08 GMT
USER user
# Wed, 15 Apr 2026 20:18:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79dec2323c1b616d1815d215235e7214217786ae0cdec9018d33e3353158ebd`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 9.9 MB (9904377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef3d3e089ce4f1f0cdea10454197d4b856179f93b0881b1fbbb2f6d7bbe9752`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e9cf0ea2e20131d951f7eb3c8e90d027f05753b06a06284adfc24591741c25`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 5.6 MB (5643320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:64e02ba7169fe7427d2a843f819239f3bb4c285582557fc4bb8e8f9e9fba3d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1326824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ba9b7cba5ebc56e832b06d9991bcfde287164a0487b199f6ae9318ed139db8`

```dockerfile
```

-	Layers:
	-	`sha256:1013866b449ede3436fa97b85a19bea88d8cbbfe27f2a350005e2b95631571a5`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 1.3 MB (1309192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea2f3499ce7de5710ce312145acb7bae5b22bdfcf5875b6a84b6aefae38443a`  
		Last Modified: Wed, 15 Apr 2026 20:18:15 GMT  
		Size: 17.6 KB (17632 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7b9894af2ad3e75a6b5e643c310b097562a2a87c60247f4c0de46b219a0ea5de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20932992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723908ef497f2f1786ea7c7a4b275b9864bd678863136e6a6c6ae49f5c87e0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:03 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:03 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:03 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:16:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:16:17 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:16:17 GMT
USER user
# Wed, 15 Apr 2026 20:16:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3764ce07cb9fb07911422ef3e80f2f06c0f31c885113098ec8b13c160905b584`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 10.8 MB (10795637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1634788c728d67c110d9d4e0c15ae13b2e6b7a80a77ff3a878345213d581ce`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07c53b7b681fdb25c1b58692718b42d2cc2b31317e0ece3b3c0c380d809367`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 5.9 MB (5936500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:52701cb1c00bb28d537acde50c49ef4784ec8a482bdd8478cce4e7bd572ee4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2179829906c4a8910ab9e20abad2f943a493fca28c0be75620b92566a742e914`

```dockerfile
```

-	Layers:
	-	`sha256:dfcef6d50e20c567b12b21284967f6ae37c8a2073fd8fe387f4aec8cb1483826`  
		Last Modified: Wed, 15 Apr 2026 20:16:24 GMT  
		Size: 1.3 MB (1306238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d84bee390fe98a360de40e03f2681e268921c47765fa679b33ee75fc08b6af`  
		Last Modified: Wed, 15 Apr 2026 20:16:23 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:b3be93716c332caea0efd0046cc0e1bec7c1869fca4821e1789e1042607652c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20226813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806f375f632e375cc393636cd0cf194e1417b55dc702350b1c7e989df95f3bf`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:20:48 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 22:20:48 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 22:20:48 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:20:48 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 22:21:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 22:21:06 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 22:21:06 GMT
USER user
# Wed, 15 Apr 2026 22:21:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b20561f93fbd784885928a7bdc5496cc351d13ba590d7677906e332db7dfe`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 10.4 MB (10390987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2899b7c728e3786919f78f216c3cc06314662cc7a39aaa46d5a6e52c3df73c`  
		Last Modified: Wed, 15 Apr 2026 22:21:12 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955bacd8728c20067a5cc2b25b87df5ffbc903b6a939de5d0a9c75d647d9fb98`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 6.1 MB (6144398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:93ce05abd87b658f33a303d2ff604976901153ce174e9016ab35726d3014bca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1324183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbdcfd6a9387c03db734beaaffcb335ed9ab7289b8e1ea3b676578476a5388`

```dockerfile
```

-	Layers:
	-	`sha256:4ceae1c6bf79b1c1e63914818f6673c06d6ab4174d52fb1f3b7cc2ee1f8ba46b`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 1.3 MB (1306739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62bef2452b6c6f240a0ca80a588c10c66294d389ea7f48156bf1ed1a446dabf`  
		Last Modified: Wed, 15 Apr 2026 22:21:13 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:254afdc9663a28ee737288f82d016a19889a7c8754baae69395f2d17bfaff029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21274213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2263772125383f143b80e6be1c94a04db51de28777edaf65099fe747f8e9786`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:51 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:16:52 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:16:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:16:52 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:17:14 GMT
USER user
# Wed, 15 Apr 2026 20:17:14 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb8acfc73a055a737970c574659149b8b5011cb66a2471181b70b4545ab061d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 11.1 MB (11080147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cc343afa57def6717e37a31ebd9c0a3f96cdaab4fcd6fb77fe09d0928a4f60`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2ee35f7d08e3f891969387cf3d54ce04ad6f25b577b354c9dc65861976e82d`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 6.4 MB (6362152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:dd670c211672c1ff7f437ac9de7554f3bb7d5b31aee4bc25d2f6daac8ada855e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8985b9021b635d6db90b26530a7142ef977f9ab6b5ee00d73682132aac50f`

```dockerfile
```

-	Layers:
	-	`sha256:61c46e29cea49bdaeb4579b4b32f590dd09ade9f7babb0e92937336be2369626`  
		Last Modified: Wed, 15 Apr 2026 20:17:29 GMT  
		Size: 1.3 MB (1306191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04b155fa69a2f233568615ccf2b447061dba7c85665b73d2f8d13b51f17df5e`  
		Last Modified: Wed, 15 Apr 2026 20:17:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:bfb4fc15f5ed90f67fd76e60601a679aceee8d624a9cebb62c3467a053497187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19943959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77108e163255a50f7eb48818727d6199fa18870afa211283ed5c516f65705898`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 23:40:39 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 23:40:40 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 23:40:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 23:40:40 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 23:44:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 23:44:28 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 23:44:28 GMT
USER user
# Wed, 15 Apr 2026 23:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3876ea28a626875613089e4c0154d886493d2978e5878febd20db5b52b40d2`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 10.3 MB (10291169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa98a76790d03a8cc0c25f479195b0c473c021cd143d9fb33022b3e6e2c094d`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf07524a0c6cd9050b930be06bdb1518111677f61a8f28dd8ad0ec0184265c`  
		Last Modified: Wed, 15 Apr 2026 23:45:31 GMT  
		Size: 6.1 MB (6064142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:4cc92eb4b78ca33cac771f363db2ae54762f45f6e734f21a4e01790bcc4daae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918ab08cc9d848fb7ce9c1ffc1a4ea4e331f579f7c7128a7dc421f604281899`

```dockerfile
```

-	Layers:
	-	`sha256:711cf3d984876c007cd510a22a7ada0bf35ea70a789e863e81db69d9e382a1c8`  
		Last Modified: Wed, 15 Apr 2026 23:45:29 GMT  
		Size: 1.3 MB (1306187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c69a7d6857546446e8284d168ca983d23255b2a89e9403e525b1ecdfa308d70`  
		Last Modified: Wed, 15 Apr 2026 23:45:28 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:3c8ece34a2fcdfcfe9d06fcb0c9cecb6620f3df146180789497f2f60e6ec9cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21334454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424937e538e09808772e1c933bdfc98f7e1246703af88eeb73a8546ff78898ca`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:14:38 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV HOME=/home/user
# Wed, 15 Apr 2026 20:14:38 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 15 Apr 2026 20:14:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:14:38 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 15 Apr 2026 20:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 15 Apr 2026 20:15:00 GMT
WORKDIR /home/user
# Wed, 15 Apr 2026 20:15:00 GMT
USER user
# Wed, 15 Apr 2026 20:15:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039c6078db85a63371a551471eed0c3ca92837a3efae9929f759f4f2ab304005`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 11.4 MB (11403564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c23488248c4834815a024dac0287469c4e0c3f509e1d6601dad9ebba3ae064`  
		Last Modified: Wed, 15 Apr 2026 20:15:15 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692f8d5135249c4b910046ab77a1a059df863ff0a74b77329ad64f860e74aae`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 6.2 MB (6203373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:90fa0fa19724af68aca64e6da748c22d2673878a7982be79fbcd5e5457ff42ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1323632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18dfc948454050fdc29c101ca6089e0da0689c3259f3e6903686df6ea40ece0c`

```dockerfile
```

-	Layers:
	-	`sha256:8bee6112489a71896cbc2c463f534c78d0bda9c15d98e590ca17ab900f0a7661`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 1.3 MB (1306133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e2ba4990565e2b2c96183c5443f41b0a2c2c8e498c6bcb7d6e476180234cef`  
		Last Modified: Wed, 15 Apr 2026 20:15:16 GMT  
		Size: 17.5 KB (17499 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:5acc53eeb8b33947406ddc481d5fb68e9d285406df75217e27a0c4aa441ed705
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
$ docker pull irssi@sha256:88c0ccf218b4a0588bd739e0e6b36bc3627b2c2bf6ad7c878b9339310029eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a432ec7f4bc3a819553703167ea6e60f03085a1421db1308b36379f23bf407b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:20:24 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:59 GMT
USER user
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cbe811686f30430463194903c8403046a46e2cfc7863672ddaae3ea1de9ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 19.2 MB (19222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef6fc2375668881f03374a60e1e53c054a2dd9fb7d0d89d2ed20263afffacf`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066b975499f88330791f13923102ac1707a92bf511329cc8e953ac9506d06ca`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 4.9 MB (4866901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7e516331d2e35431375fec60eaa42df6ab7686f689de4d979c90297b074e8d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74664e26abe8c4bdb5efdaf62508f72ce2925a79ef9c7a6f18eedd3acd93cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b917b983fdd6d74b71df372114b8be6d79be535d12e9a231fb2de9298ea11f6`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090405506a1e903055a1c09f043bf011e58cfa6b6f9bac0d3a9a88c1343ddd4c`  
		Last Modified: Wed, 22 Apr 2026 01:21:08 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:5acc53eeb8b33947406ddc481d5fb68e9d285406df75217e27a0c4aa441ed705
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
$ docker pull irssi@sha256:88c0ccf218b4a0588bd739e0e6b36bc3627b2c2bf6ad7c878b9339310029eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53872792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a432ec7f4bc3a819553703167ea6e60f03085a1421db1308b36379f23bf407b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:20:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:20:24 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:20:24 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:59 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:59 GMT
USER user
# Wed, 22 Apr 2026 01:20:59 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443cbe811686f30430463194903c8403046a46e2cfc7863672ddaae3ea1de9ef`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 19.2 MB (19222360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ef6fc2375668881f03374a60e1e53c054a2dd9fb7d0d89d2ed20263afffacf`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8066b975499f88330791f13923102ac1707a92bf511329cc8e953ac9506d06ca`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 4.9 MB (4866901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7e516331d2e35431375fec60eaa42df6ab7686f689de4d979c90297b074e8d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b74664e26abe8c4bdb5efdaf62508f72ce2925a79ef9c7a6f18eedd3acd93cc`

```dockerfile
```

-	Layers:
	-	`sha256:4b917b983fdd6d74b71df372114b8be6d79be535d12e9a231fb2de9298ea11f6`  
		Last Modified: Wed, 22 Apr 2026 01:21:09 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090405506a1e903055a1c09f043bf011e58cfa6b6f9bac0d3a9a88c1343ddd4c`  
		Last Modified: Wed, 22 Apr 2026 01:21:08 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:370fa6c460f0d93d5292636e450cbfe5e93417629805953fd12346a9234576b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac73bd2fad0eafcf80defafcfd48d78937591527bcb48183cfbc0d3bf258743e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:17:44 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:17:44 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:18:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:18:39 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:18:39 GMT
USER user
# Wed, 22 Apr 2026 01:18:39 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0ea9f3e87ebe5bdbae19e83cd0492784446e35f4fe723cbaf0daaf1fcd429`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 18.3 MB (18293813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c23f18eaf771b093288784e640cff2bb713f6aa2469037e40fed309cc3580b`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9f6ef4819d6080f8d66580b307301f8d9be1d2d8b69375e96560a0cbe4903c`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 4.7 MB (4709755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ca2ff24182968b24dc9b3c5e6d89b28110878b978f5916db7cbd5ecbcc3f8f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957623ff98ed3ee76c6facefd0280daf7f922742dc590be8b75d4c13126d4a24`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f789ddd33e0b73c16eb98a5a23c8dce98d7e801fb90eecf3a5e3bb1840f48`  
		Last Modified: Wed, 22 Apr 2026 01:18:50 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d907ded1b7b92c39be232f36e8282489e050d6bb1ab96615b2ec93c4a9e401`  
		Last Modified: Wed, 22 Apr 2026 01:18:49 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:71e41e28108d0aa55876b15a52bf920d6d977588447766d1ccb187a55246df6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48689616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db860102c1161ddbc2030786dd2636c59393d9705c71f62d2952710c43abeb7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:15:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:15:09 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:15:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:15:09 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:15:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:15:52 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:15:52 GMT
USER user
# Wed, 22 Apr 2026 01:15:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e762d4189f613fc787b0748fd699310d53221d361475d09b04f2a64edf3b5e43`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 17.9 MB (17913215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457b8475e8da8ea101c210f56900da8f711d5df8959cbc324c6875483c4e9028`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ee8768d81048997d2d0119d5adbc9d72c9c00bffcd1d6fed437dbee8a17557`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 4.6 MB (4558200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:62dedd49943664b2047cbce7fa555974e068fbf8870ac02f0816fe31b90f8f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c8125eaf7e934f653cc0b01af22954d0230124c02cb5cc87801fc3fa8ad206`

```dockerfile
```

-	Layers:
	-	`sha256:7ebfeb4df85b8db212f829cd9880751065dbf89b9f159cee78931c525bc0f3be`  
		Last Modified: Wed, 22 Apr 2026 01:16:03 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33cebc4b1ce0ecb19f05e9bb1a260660b8c83bd27154e41a116d920eb134a926`  
		Last Modified: Wed, 22 Apr 2026 01:16:02 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c3be7544b98c62673029731e6664fafeb72edbd3a99fe936e9d35f6e2cda6bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53978722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b238871944625cc61286004daf2d844da7d9dce33ad1aac0e7ea652a741e6d4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV HOME=/home/user
# Fri, 08 May 2026 19:19:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 08 May 2026 19:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:19:47 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 08 May 2026 19:20:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 08 May 2026 19:20:24 GMT
WORKDIR /home/user
# Fri, 08 May 2026 19:20:24 GMT
USER user
# Fri, 08 May 2026 19:20:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ed2095b4c0c8aa1b9ee3fcee4f4da7fe8b9fbf6b9d12631b969214e493165d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 19.1 MB (19050085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2804b1373a8cfbd97b2ae54297681aef493b1b413f1383da7c38ecc392a40ecf`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80010303ae5c0355056c47e42fa009f06a6ee193e06c3803a0cf1e48a368b30d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 4.8 MB (4781632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:270a80040d768fadd72f9413894a8ac4be9440f205b98482b89c4235eefdfa2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e2c091a876656c57b7aa0fe3d4da650a9f54fe18e821fc3c9f0f17b9c54f1f`

```dockerfile
```

-	Layers:
	-	`sha256:938c18cc35595dbaa89a2e50df95477fffdb87f67cc06b1377274e023b7599e8`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef9f4a9a29afe95742a95d4bfa35a0d64f8a9a012f971148da3dbf1e3bd3d7d`  
		Last Modified: Fri, 08 May 2026 19:20:34 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:055b29ccc94873b4b54b99c70dc918ebb2b620dfc062b9a3036ef2c232622109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54911311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e517d9297cddbd7b1d2219449f4c98f8ddb5090f362e2f605428b1edc73d7aed`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:16:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:16:33 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:16:33 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:17:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:17:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:17:15 GMT
USER user
# Wed, 22 Apr 2026 01:17:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec744225633eb6a4473e2ddefa9947f6b71816efd439d0e446d922b36ef2e08e`  
		Last Modified: Wed, 22 Apr 2026 01:17:27 GMT  
		Size: 18.7 MB (18743203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af7ae311f82f46fe32b246c10278b0911099d6c47440e9034789a1f6c37c411`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b66d24e88ce31dcb18eed04f101927b13e015502d3e90b263580be30bf583c0`  
		Last Modified: Wed, 22 Apr 2026 01:17:26 GMT  
		Size: 4.9 MB (4868424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e78c0bb279cfe5f6e85848c8f46977bfed51a74064aac682113d7c762abad68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be84b5416e00d109c5dcef73e47d3ff82e449d1318f82800594cb00cc472ef7e`

```dockerfile
```

-	Layers:
	-	`sha256:e9c263afde60a9332033fab956d046f9996609356afd36cc5dab045fe701ad25`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c56bd96c8a2a168c26958a05b291d91418289cdff71063f5605c6bf97c61ece4`  
		Last Modified: Wed, 22 Apr 2026 01:17:25 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:82923657e03e6163682a32677c1a10e331f271b36c32f99fe22c5132028d7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05d84bed09b679963357df213875a904953ea7c68220576787ab66b610bdc97`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:28:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:28:04 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:28:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:28:04 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:30:15 GMT
USER user
# Wed, 22 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e3b37d6ebe0eb9859eab96898a22149e407d5a85c7f2fac3a2a5642d22a536`  
		Last Modified: Wed, 22 Apr 2026 01:30:44 GMT  
		Size: 19.5 MB (19538525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf8c1413d25025fcd20ffe57d5c8307e3971824661a0446ef9883c420eaae37`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701760a9539f50d19f90cf9b936383a9c0efbfee27f99021ea9fb32b15bb5a67`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.1 MB (5097824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4093f2f1d2c5a56e27694586e991f1cb36e274f55c4ac4ef3944e8736c6b9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac76e7dcfb17fc48104426901645920606c304b11f1f2479580a5a1d184004ef`

```dockerfile
```

-	Layers:
	-	`sha256:ce5a8ba40da6828458087e626f78d91fe5a5342b41dcdf253e555295589fb868`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a11f70350e32f4934d6db0e8243d557d27fcbbfcbbddf89259203cf3f498dfa`  
		Last Modified: Wed, 22 Apr 2026 01:30:43 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:849889b627b035af5db9fdb41eb995e0c8aa187e265f40a103f34df45433a314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66082132229be6f28d63805afb23b4266b6b67aaed2f4d2c938bc8534833f00c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 08:19:46 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 08:19:46 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 08:19:46 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 08:26:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 08:26:32 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 08:26:32 GMT
USER user
# Wed, 22 Apr 2026 08:26:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61aebb695a18cb63f88dbaa7d0af9cfd4774ed90c2d0135878c5f6c4013ca512`  
		Last Modified: Wed, 22 Apr 2026 08:28:25 GMT  
		Size: 18.6 MB (18554801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407605d1e830d033b8318c862350eac8c9b2e00ad358377600ee252cd964788`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4283203cd42f868365c4c23020e4e0be3c2706f2ab0a3bd453e02a8a30da62a`  
		Last Modified: Wed, 22 Apr 2026 08:28:22 GMT  
		Size: 4.9 MB (4860733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a1de1864e81714e4eda6f97bda6f52d3775031df95ccc42d00e6b256081da905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f030f4c0b97fe11fa1b877042e7afbd8930e18b996fcc2f81a6340b1a5ff81`

```dockerfile
```

-	Layers:
	-	`sha256:89eb6ee8d741cc41eeac55830202bb13b835f2b483bb458eb82d6a85f2c89f93`  
		Last Modified: Wed, 22 Apr 2026 08:28:23 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf65abe22e2235b74a6cc5c30de46bfbb9981bce5e914385680d99eec9c795d`  
		Last Modified: Wed, 22 Apr 2026 08:28:21 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:5d22bb98d91d0bc1eddfe36a55d1d847332166d66b600d413e25287a2f44d7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54518353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4555d501fc9397be1a3d3487d7ef030fca5139b7bd06ea7de4299457e3e29d26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV HOME=/home/user
# Wed, 22 Apr 2026 01:19:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 Apr 2026 01:19:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:19:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 Apr 2026 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 22 Apr 2026 01:20:02 GMT
WORKDIR /home/user
# Wed, 22 Apr 2026 01:20:02 GMT
USER user
# Wed, 22 Apr 2026 01:20:02 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6739e451136222b031c62f849b66f2dfd5a6dc325fde7f03fc424c4c961cc91e`  
		Last Modified: Wed, 22 Apr 2026 01:20:20 GMT  
		Size: 19.8 MB (19768750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf36fa436085556ef4ff4608e6eb40a8ce77528da8ca1d3753642a3917f3867`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb61b2aa409ff7a31af28e3509b85f17ec562e4d343107a60f270b01abb392`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 4.9 MB (4905945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4636b6bc7aa857b1d956e849473f3d2c06c45f86bb7608c707a22fb2cc039068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769361312ddcf695b1cabf8e205bd1489e68a760ca64451550dabfe5de4d7670`

```dockerfile
```

-	Layers:
	-	`sha256:07d88d02e9b19d48033784c1a1f293c8535ecf444fdfdc74da43935685fa68e6`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7aeb3018311a7aaf0d68736b7781ae962dbb8849e7a2f87d90a0002253a5bde5`  
		Last Modified: Wed, 22 Apr 2026 01:20:19 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
