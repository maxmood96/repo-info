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
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
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
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
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
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
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
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
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
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:ac5ef39f4872713930c35c21217527ec8b66fe8646d0eb627c54f68a08a6156e
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
$ docker pull irssi@sha256:d6648063cefbd933c29ccd69e16863b697f8a9d757707c07451f9dc1d1e1738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5aef6f90866c709c50fc249c70106c545f0cf0628474103ac6ccea91d79419`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:57 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:22:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:22:34 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:22:34 GMT
USER user
# Tue, 07 Apr 2026 01:22:34 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73ec966e254c415ee80da3ff701f1a3785035c1efbddeb8d00d69f611da4ce2`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 19.2 MB (19222726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbdcf14e20f138271fa4cdf5f714f77ab97bb6c10941b78903d5fdb510e0d5f`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98db67b9ef4e1b7e9f4ae5c73c0f6301e4ad79cd5d8687581a9b82a809d90e5`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 4.9 MB (4866892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:710eeaf25265646aecf7c3eb33b36dc466c6c4bbc49e5ee1dbc3c582d621b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f8ce8b91c7a779f2d19957d623937f77a50d6dc3184aad9b4dd4cbae918e73`

```dockerfile
```

-	Layers:
	-	`sha256:cb44fa3531ac77f35745b9812d60aa5211c76afd077013efc945c4e9828ff70d`  
		Last Modified: Tue, 07 Apr 2026 01:22:44 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a1782e44033d37606a3812a4cf3487ef4eddc661df7f27176fd14a4e53badaa`  
		Last Modified: Tue, 07 Apr 2026 01:22:43 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0ff0211a99fc58ab3e2d5a5d31cabdcfc46acb06fc34cf9f39d041bd6b71b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50951095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f401e123e813abeb1f0157111ff7f698e7ebaf2cce27fcab853e9f702cbcc596`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:37:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:37:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:37:03 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:37:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:37:53 GMT
USER user
# Tue, 07 Apr 2026 01:37:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e82b3664f07b19259bc808de301ba0ea8e4d5df899d8cbbb0d82ff5a03956a9`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 18.3 MB (18293874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15c5eb53d9815916d71522faa6af78054ee422099d6ba0f26af029522f4257`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc28f01e63e11e6fc98fd56f3fd36fd33119febb269346fccc2f72ef6bc5e3`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 4.7 MB (4710048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:595e1bba58f640a7844a1a06a8d0802f813a5d9f8368e4969f6a00f898965718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bfd0ac08f1d92360dad7c6e9f3918a4fb76c674d74f24ae1c8f0cc06979a4e`

```dockerfile
```

-	Layers:
	-	`sha256:c03056c254f4a32318a8dac3334dc12dfb370d041359a67a88bb0c560c1db6ce`  
		Last Modified: Tue, 07 Apr 2026 01:38:04 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072487f5abed1a6667772f7d03a5d1236dffa7261c3b6adf0fbd06e75044ac06`  
		Last Modified: Tue, 07 Apr 2026 01:38:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:4cb4198ce350f286862d53504d9725ac021787fb2cd9074cd5295b74c8484cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b096709170112bcafe32b93db05fa05c04d8536cf2ae06ffb46faa7acd198887`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:25 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:07 GMT
USER user
# Tue, 07 Apr 2026 01:18:07 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa19147081a3f3405f04a7c5dce94280e6ce43c8ece2b9d55e29b4330db5ee`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 17.9 MB (17913346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe597540c0bb5fdb7ee6f9f24f48c75153eeb6e0514d3b60714c63da0335bde1`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60eb2adaf6b4b36733aea605eb6a2b011a38452cb7a38f36ef35a12929432aa7`  
		Last Modified: Tue, 07 Apr 2026 01:18:18 GMT  
		Size: 4.6 MB (4558345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:90450d98788a8de633d35ca193e8d4a132e719a38b8db2f75b7579b294725836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8555c15ee998296facd5294c0f788d79ae55f15aa5a18e3e38861440fafb86`

```dockerfile
```

-	Layers:
	-	`sha256:61bd48009d6f2cc5d7b5b9e4e2038abb87d97983fcd4cb7b4f4d841be9e38433`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28858e17ea228cf3e90c045dd28ec8eb53f534f0126a6edee39cc824af5abe81`  
		Last Modified: Tue, 07 Apr 2026 01:18:17 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a3dfa37ea465cdfd20a3db4ab11913c00932c783ae6006176a06a40aee0d7272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de34885057de63339b36f3f1778ecf426471e8e227fa37e02e5fa9517e441b3`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:21:15 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:21:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:15 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:21:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:21:53 GMT
USER user
# Tue, 07 Apr 2026 01:21:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d0cd6ade05309398ffafe0cdbdaf161469d04415182d437056cf3950192b09`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 19.0 MB (19049833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf399450202a5801df064342038a8263ae8ba8f4f203c6b1f8e28db80e6ac45`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1829e46517551c501298aae0289c218e4eba203f1942dd0c0f4430f17e987a`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 4.8 MB (4781490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:474c0cd954cd39f96885a586ac47543697d4d00bb87c75b27dcbead8f5dc8b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aea0caceafe0fbdc18df4cab29d4f5f3142d5b6ca005e5ad79cb0b05d9ec8`

```dockerfile
```

-	Layers:
	-	`sha256:677002cb7bdaeecf0d77ed01df14ecf63e7b60f7522e07ce827203d28e8fd9b8`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1143848380f4b59c9f616d9ae719cde295fe1889a18f963a1fa9e6ff1e1464f`  
		Last Modified: Tue, 07 Apr 2026 01:22:04 GMT  
		Size: 18.8 KB (18831 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:ed5ae6188bfbe886acc051140c365f38b36b5b88137b8a892c87e308a8644b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221408b41c5d46212179597cbed96211525393ac69a67ae3b46a0b7d145b9eb4`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:17:56 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:17:56 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:56 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:18:38 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:18:38 GMT
USER user
# Tue, 07 Apr 2026 01:18:38 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1068517876c9872b98f086119e2a62e7640e7cad9276b8d3da806c5e6300bd`  
		Last Modified: Tue, 07 Apr 2026 01:18:49 GMT  
		Size: 18.7 MB (18742892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91c7e25281e19132315d24bf5c42698d217000660dc21968f97a7dd90f3107`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6c379b394bf5bfbdbde1a7a9ba97079e560b8183cf6c62b85ccb805eed6e22`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 4.9 MB (4868486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:e765db21cee389d021cf4eb70a3ee12ec4bdc7485146277e5d2e8416820d7029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf872a3f53b32c3aa28f519f1f920a31427c1b152c3e7b23f6b04b299a042342`

```dockerfile
```

-	Layers:
	-	`sha256:45e6232ecd658f71029f5c87c178a00c507521da6fa9560048123f6fd97f9863`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12123be1e36867174db57e80045d36cf073142edc27f54da25667908877a646c`  
		Last Modified: Tue, 07 Apr 2026 01:18:48 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:3e0cdd15c9e3689b9e917dd50d4d3c722637c576b5ae8380bac06d06bc7e51e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaf8ae12f9fffcf217a1c9d1febb4e08e6a2953dd442aab6363417e14e308ac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:28:27 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:28:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:28:27 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:30:15 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:30:15 GMT
USER user
# Tue, 07 Apr 2026 01:30:15 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e441d528cbe3fb7d817d13c1ee44b0891bc7221b169663c5de196778c327ceb8`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 19.5 MB (19538902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf50cebbe7295799d98dabd83d73b93437d4e12bb95f6e91992a1096f9f9700b`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c701e67bc76a234e63e9da56c2752640c968ef3a67efbfcb3147a9ebf789f`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.1 MB (5097861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:32a28d90cba59e8aae9e58c09ef3c2e07069ffefc70c1c1c066df003b3cb427d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6302cceb15c2c5f49e1d4b9c9a810aea48ba60b2f8c2eb63873d5f6e38dda1b7`

```dockerfile
```

-	Layers:
	-	`sha256:75bbeb8bb0ea51cf3ffa2b9534f07978bf5a3e12030f2f0d133dd48e88317c41`  
		Last Modified: Tue, 07 Apr 2026 01:30:45 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe3c7716404f187efd488051ad98daebe9780702c235dada5a4f3374adbd69e`  
		Last Modified: Tue, 07 Apr 2026 01:30:44 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:de75ac83844d16a431173c24ad2941ef0bb77e2b50158f548ced270c715a8056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415465f2c0431fe2f20904aac8c837745b099ea8a1b42a11ba5b19c92b201e75`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 04:50:18 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 04:50:18 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:50:18 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 04:57:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 04:57:08 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 04:57:08 GMT
USER user
# Tue, 07 Apr 2026 04:57:08 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f51f26f8d0592eec96865265f56184e8f402ab8eb81f835dacd4401cf5147ee`  
		Last Modified: Tue, 07 Apr 2026 04:59:04 GMT  
		Size: 18.6 MB (18554914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e8445be92a7477f7fd1509cf4995f774c78733242ad8d02f3c9cbf52af2ab6`  
		Last Modified: Tue, 07 Apr 2026 04:59:01 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b51f0b1c8335e312bf7a23c47ae2cbc36839c30fef38c489874292f14c550`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 4.9 MB (4860744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1fd6d48d9641d2c96a03e537aae91266cc37a0292746617f8dbf04d547e48e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacc3f5e8506a9bc50b06804a3592298c344685d275da00c08dda107aaef3f38`

```dockerfile
```

-	Layers:
	-	`sha256:c2930c027145b45aa97fdc5180f7d4687767d41b4345fb118c6ecf53ef3efbd4`  
		Last Modified: Tue, 07 Apr 2026 04:59:02 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b88688c25fb06e61ca2b0bb556970657656699ac09ca2a30d47ca434c3a08040`  
		Last Modified: Tue, 07 Apr 2026 04:59:00 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:79b728f0e7e7d44d94822c52d4609d9150bf5e20896cf9e154dce59e0bbf8dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54514101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca792363cbf7feba8477897cbfdee5d1882b48f2a7e154b199d67ffa926f5cac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV HOME=/home/user
# Tue, 07 Apr 2026 01:24:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 07 Apr 2026 01:24:02 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:24:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 07 Apr 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 07 Apr 2026 01:25:21 GMT
WORKDIR /home/user
# Tue, 07 Apr 2026 01:25:21 GMT
USER user
# Tue, 07 Apr 2026 01:25:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ee55e9e07cac6e6c205758868954c4b0de8ffddd5189047497e8cebe951d45`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 19.8 MB (19769041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6078a9042ed0e81877710e7436e602ef3c95df91f552b77d6fd1a2eeac86847`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccd5e98a0afaebded0b419deeb8983fbb8b31ef92132448f31525145f366dc7`  
		Last Modified: Tue, 07 Apr 2026 01:25:42 GMT  
		Size: 4.9 MB (4906277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:768766e8967b012b7e9364ea01b3043fd1f73909355a397df11bf6346564132c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f55da68e4d8d5696570c91b53f261076c4e5e3d6630397e8bf1d8814b0b6b2`

```dockerfile
```

-	Layers:
	-	`sha256:d5c4c9b4aad6807be9d435f9ffaa4da68737db4dbbc3c84c6649e0ff6418b40b`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46254fa5a9f034226fe4012acf21f29769f40ada650ad5e59b4fccb16ece6cb4`  
		Last Modified: Tue, 07 Apr 2026 01:25:41 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json
