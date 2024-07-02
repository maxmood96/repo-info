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
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.20`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.20`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.20`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.20`

```console
$ docker pull irssi@sha256:24337be1436c4487c5e23941cb7a6b29ef838c67fa288960b89912542dad6aa1
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
$ docker pull irssi@sha256:2da5a616146a6dbb4d600574c1c6d81e5785d37974628b5aad0966f2cb763a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19726156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857cbb2f3ee4eac134944e62998c9bdc90423436668ddac18650d2ecb7153052`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6771043bae2aa0084ba59f155d848ae366cbc868da4b7ec1b82be3fc14f425f6`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 10.2 MB (10194211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c63e94b7d8717b59271cc88936808f71c3bd0ff89f13e6c58591ec3cf31f34a`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9baee14fc5afd50fc18b3b2c380b557c8ca39c3caf8f7ff995c0e1c5f053816`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 5.9 MB (5907102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:0551fb90aad90b2d15ba465040d3c2dbc15cc526645daeaad4be01259999a0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcccdab3d25c2b1919402d88f3af5db15341e72748468e5b654ad1a05db13cd9`

```dockerfile
```

-	Layers:
	-	`sha256:98e4c00f3a40324b1f8bc2ddb07749df88377371572ef6a1d3f4ec9838430890`  
		Last Modified: Thu, 20 Jun 2024 20:56:20 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:b38ef8bbaab67c35cd04d0ea21d8095249ea847904196b790a6f9f16e66635f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9222704714d16027bde19f6274553a1e98faf342b4646c1ba13c88868fe4dbaa`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d1145e18c577b1b5fec17d5877f4ccb46a61482f1f3a49406ee1366bf4400`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 9.4 MB (9362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b7401ebe4486150bd416663d913d3053f105fd73073b96be119c77851e65df`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7d1040386cb9aac87148406783c7d98a536b05ebbfca8bb6f02ed4a2d2002e`  
		Last Modified: Fri, 21 Jun 2024 03:42:23 GMT  
		Size: 5.8 MB (5750386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:178cb38fafc3dce5f4b3fbb9aec837844f3f88b8494f65121830becdafbc20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ff4ad5dc78d03bd087bf78a69ae1a5e2bf0e6bc18130972132319afdcaf752`

```dockerfile
```

-	Layers:
	-	`sha256:19afc8d98c790f76232e11419027c6657066507c2b20acb2d60fcd70af6e7996`  
		Last Modified: Fri, 21 Jun 2024 03:42:22 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:013f243f6402cfdc9a9c2026775a10e7a930f1e8f786c6123d8190a588900499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17783704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05c68c669f7fb7930803ccd73bce58ee28596d80f75f930a1cd432d571f30d7e`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaee6ead174507e7258ed2c8245f092dabdaca2f3442980d860947368c6b036`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 9.2 MB (9185698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3576cb29206c70451fe446a98bf6c6311e2b2eb4bef57971917a67f39d7f1ac`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19a766c79dba3373b1c84f63b2b9d8b8de54f61a5d09369e9c39785a2ebf51`  
		Last Modified: Fri, 21 Jun 2024 03:42:21 GMT  
		Size: 5.5 MB (5502153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:399ab979d3f8372a887223b7ecfef19c0221e72e4802af240709fabea0debda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81b9eb75bb5b22ed44448a9bbbda04d56657baefff4f4c7a71f1227cf5689fb`

```dockerfile
```

-	Layers:
	-	`sha256:cb5e2e0b71c1a85989e08f2597abce122543c8156dda631a7d734a400d7b19d0`  
		Last Modified: Fri, 21 Jun 2024 03:42:20 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:8a9a4aae68c655b4bb462918d5ede6b4930c3a0da8f95dfc214dcf9cec0bd1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20055560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea0b26ba5f4f8b34e74a3b41278d7c9984daff4dbaea382f9874a61705550`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55e92ddf1d8c2fadc31e474cc310e0d97e67507e3089ac9b907dc7cc00b50c5`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 10.2 MB (10159410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da08983b535720d265b72c64cb60a6a59f3ca3e632703f3973f229ebe56d70c`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eacb4ce48aa48226b9ba9e119d8b9e2802ded226fd3db32f02b93d7ac26787e`  
		Last Modified: Fri, 21 Jun 2024 05:13:27 GMT  
		Size: 5.8 MB (5806351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:897fd4091404f549e103c0f6b6c6fe30f89de971f73eebd9623cdc0dad517fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c2ddd8825a578faf2e7e6e40e77cc85f20c850f8a0353ce2f2e54931633461`

```dockerfile
```

-	Layers:
	-	`sha256:a7569196bf788354f3ca293eedefd3fc83da68e9777c9af37552c104f15aff20`  
		Last Modified: Fri, 21 Jun 2024 05:13:26 GMT  
		Size: 17.4 KB (17445 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:55f5c2b3692b0dd39d2b967278f0fedba33ea50a03441da1e8c3b60dbe649586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19100475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299850cf5b5d0febed5285c80aa0552bb72acd403725f87447cfb24fe84499de`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
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
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4b9db8a4bb0d6ad48a762e5bb1adcd7e10b89ffa30ec26aef946a758b17729`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 9.6 MB (9636341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e916d3463220bce01ad49ba693338cb831bc488ebd24b25c0bd500b100e527c1`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72960f4c563f20285040b6433a1bc6afc686d8c535c2807c029f8d1e4d14a2ef`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 6.0 MB (5993664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:9e312b71b4a957524090af85253c76f4c53f501dceb8d95d1bed298d95f3bbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee0a7cd6a3e84e2bb406b43235d962b6802bb6659793ab6997d9c7fffd8b3cda`

```dockerfile
```

-	Layers:
	-	`sha256:54360e55ac74733655405b344aca87fb75f142f48e2511d8d9d4762bab7605a4`  
		Last Modified: Thu, 20 Jun 2024 18:53:42 GMT  
		Size: 17.0 KB (17040 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f86b17a21db761cd43a758ecc8724a318d6a725690fd9f62909ae34bb2fedbf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7ae278232eaab7ab2dc7b5235cb3325ff287f9d02f0d2cf9a2f23379241228`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4f030a3e5840fc473a6504241e09e5ae5d4117ebca5e8aa287a82b8b756368`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 10.4 MB (10379398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc9ec5423926ce95a9dddcf3eac913db03f1494412aa138871219ffd89047a`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191596ff454a9af058c7105591062c2286d7fbdbccf0105af6717d81ee683b86`  
		Last Modified: Fri, 21 Jun 2024 01:58:26 GMT  
		Size: 6.2 MB (6164926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:e0fe0e311b537a1f39b275e7625f173f738c1d8619e93c10c432094bdbd7860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d6792565bb0b6a3ad3d285010c699d8cae049d315c65cf2a6501ee0210a68f`

```dockerfile
```

-	Layers:
	-	`sha256:c25f9e7f83a1fcee60164b1587bf402446b0e6ada9d2b1bf045b8bf96d18605c`  
		Last Modified: Fri, 21 Jun 2024 01:58:25 GMT  
		Size: 17.2 KB (17163 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2fa4c01a400f397c41f8a676008320f9ac862f5a534defd4627ce23700f1066c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18949619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17c364886f2554df981ca014e2f5bfc8ba2a298106dc7e249eaf23337a31ae2`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c25cb6d9ada055edb1f2f5c95cfe8dc6a8f5e69b2e438e42361272ad10be5`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 9.6 MB (9647539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb372e6d8d0bec4da60f0075b1c44c9fbf96514f1e9f3ab2add23bae0a560886`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b933fb498f65e1b56d20c6c0473b59b0596681be366965f87729bdc20da7eb3`  
		Last Modified: Fri, 21 Jun 2024 09:10:02 GMT  
		Size: 5.9 MB (5930045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:86e7a92b9c104d4a4ed0479519b712f1a4abf98feb055cb059de5782eeeed18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fac9db3151c7e7550d56ae94c2703c285f9fe86f048820d32a66414d5589387`

```dockerfile
```

-	Layers:
	-	`sha256:8508f586359615f6d1c99ca9f9425da3ac471d8e5c70a73e4be9f2ed8270762b`  
		Last Modified: Fri, 21 Jun 2024 09:10:01 GMT  
		Size: 17.2 KB (17159 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:d9454f65f469c997e80c36c934fa03db35cef72d6afee305acf92cf7bbffbd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20275496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427935ba62d8972b2202e218a2d9660dc20209a3e3221d1ff5b01acd33de5eef`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f2676a696a9321985529e2ea0512bbf8de8df72135eed33269673bcc286c6`  
		Last Modified: Fri, 21 Jun 2024 04:17:01 GMT  
		Size: 10.8 MB (10755477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab97a6c20664c6ed07656c77ad207a70cf786cf979751565a758d5c4da849017`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fc57b385756109b755e363416c44fbe9e4a0ac70fcd7d842fa7dda1ab11b1`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 6.1 MB (6057166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bc95afc7194bef6d2186c172bf545104ff23b59e7ff181ff6e01acdc7e7837d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eda1c85716c78df3af775e9c7a135ee39b4aac0718d42c0b99048997e37d26`

```dockerfile
```

-	Layers:
	-	`sha256:bfbd374c53dae450ae04e0f183531a5ed5e337f1d92d4162c49fd96163fb26d6`  
		Last Modified: Fri, 21 Jun 2024 04:16:59 GMT  
		Size: 17.1 KB (17097 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:5d51d9b851e192e06f75c58679fcbe45169953c3673906979c25b2654015691e
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
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
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
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:62aad0564e127908e3fbb47b6d20e7a5b5e4ce578e6e513fb692ef0068d0130f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83cbcf2a668e99992f930dbee37eaedb9ba08abbe3e7086ce589363a1dd659d8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
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
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:960199db40345cde7f8521b58ad97bcf74555160e31985e9441d6f67bb43f25b`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 16.6 MB (16633397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ad5b862ff9efdd773ab5d3735a1f22c91c10a75c384e33e5e7827dfd05dc8f`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d04ed9fb1308f718eeaf24e3b0e0ed3e7ba3640f3af09c9d7259a07dba4877d`  
		Last Modified: Tue, 02 Jul 2024 13:18:55 GMT  
		Size: 4.3 MB (4299053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9cdeb625e981c58502ca54ef094cf5f57105a3f6ea96e8395a6eb887a471b239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428c16e4f9d2581cd5a956644fd2ffcf05b884732d4dbf494bd07c01ef73eee4`

```dockerfile
```

-	Layers:
	-	`sha256:cc788991bed404b6e1254597affdfdffcfbf84b03c8ed4a35a03bfa75030a24e`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 5.3 MB (5338192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e1112b107b6424ea67726cbcbaf62cbb93e044677d0d6785a17699774f419d`  
		Last Modified: Tue, 02 Jul 2024 13:18:54 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:60f21727b830c79161a85ed28e9119672f6780f1ad98945d611d8b487d39eb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51715643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f83862d4e34597ed97af67cc2711ef200d0acc8e0c3e1a1d4f42379299a55f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3017f736f2d0132c2c36ea49ca36860f96fb6dfe75e9839fecd958a126db6e`  
		Last Modified: Tue, 02 Jul 2024 15:17:49 GMT  
		Size: 18.0 MB (18042665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3457a55c07f32a36b4263690944fda0adf60dc8997617e14156eaa2263b8b350`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e27942f4ea7cabff4e1b8896fc82f00da65dc5bae6580422649f56de81633cc`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 4.5 MB (4513057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f4b7ee67512b7d07ff2e378f946ef58087285962d8679a28834063703be821e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549d4710c1744cc1f94bf7805f7ffc4394082dee4d3d8ac3c7afcd7176aeb507`

```dockerfile
```

-	Layers:
	-	`sha256:caf862cb54e1515d8d5bfb05b9c9456f4579b86aba5cf7ff184ee43521201a29`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 5.3 MB (5343320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b65c39edd2579075806125efbd1561d430d431c393222ea3da0d87148b67c3`  
		Last Modified: Tue, 02 Jul 2024 15:17:48 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
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
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
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
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json
