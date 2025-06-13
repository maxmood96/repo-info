<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.22`](#irssi1-alpine322)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.22`](#irssi14-alpine322)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.22`](#irssi145-alpine322)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.22`](#irssialpine322)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:435eb0e627b2c03f3771ec1863901369fc0c55417efe975c0f4665a4db4d212b
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
$ docker pull irssi@sha256:c78309425463b7b98483a99808028c18223162e1b4e0fc08f4acf3d5185e5125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51056573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bfd17e927ba159c48cef3b34ef600af1895223aadee3bb2c1e8f912d8d62b3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c527eabd9ddc4a328f3d9a85bdfb58f4faeb145137401a12dc39f4bfb161393a`  
		Last Modified: Tue, 10 Jun 2025 23:28:38 GMT  
		Size: 18.2 MB (18230328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ca868d8b1a5e69a8399d68be8dce360dbd28db21c8e29cc5d265b3325c41f5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b17dd62e293d3236b70116bb2ce45df643b8b3f56da3a2a2102ed0e7e731dd5`  
		Last Modified: Tue, 10 Jun 2025 23:28:37 GMT  
		Size: 4.6 MB (4592763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c58f380b164e1d39c73e9f2e443640a34bf706b8090b5b23e86f17cb7f29538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5558679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5874bc2d5309cc30db517717103053d0d5acf3be6ceac08ed808bdd511237efa`

```dockerfile
```

-	Layers:
	-	`sha256:d86858e4ce4818847f6b0249532f2712cf39eec4bf728e295a0f1993d2608d32`  
		Last Modified: Wed, 11 Jun 2025 01:59:41 GMT  
		Size: 5.5 MB (5539964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af64def490f26e9d61cdd637aca763e387f47dc4ebfb553546be28f6f78f388c`  
		Last Modified: Wed, 11 Jun 2025 01:59:42 GMT  
		Size: 18.7 KB (18715 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6da2b1cead38b3c656f20023e0f911c65e83be433e9282736c3060ca6777b576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47224488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef44e5315de23ebed88cc1fbe236edde1991180d32cbb4bbb090906a2ad70ac0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
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
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900879b9b0fd1ed9b73ae5ff929f81a4f06deb0fb420a748443848d76470669f`  
		Last Modified: Tue, 10 Jun 2025 23:38:50 GMT  
		Size: 17.0 MB (17014043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cd0805f18288d7fc15544c959bc888fd09de6b9d3f45da6fdaab39e74cd505`  
		Last Modified: Tue, 10 Jun 2025 23:38:48 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf92caf19e04a5762667c9bf02e1dd9372aca93fb216999a11f72cbbe0c2b81`  
		Last Modified: Tue, 10 Jun 2025 23:38:49 GMT  
		Size: 4.4 MB (4444696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9a65c35ca7a4841cfe216a3bbb2829001b24addcd31f54cc5644d5bfa1baf5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984231523c38f8f59a3416c26fe558a23d15b6e3ca6546ac4529b8282811f887`

```dockerfile
```

-	Layers:
	-	`sha256:cbf5a86ba1502f2498d12c83da440114b4845a0aa1a5f95e9c9b33d91ee673cc`  
		Last Modified: Wed, 11 Jun 2025 01:59:47 GMT  
		Size: 5.5 MB (5541881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0d1c0bbbc7ea483d496db20ced3483769fe82e18061e3cddeef66384145201`  
		Last Modified: Wed, 11 Jun 2025 01:59:48 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:de01e8e4038af4192722f0f6afdc9046f00a9520cc703d80ffdddb39f51148de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44843499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c684cdd62ae2835898b756ec2486f512b4dfb890996c3f8025129899e35f95`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a3a7ce9ef204a44690a67412fef5fad23046e051c492503cfc35aec793aa9`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 16.6 MB (16602241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d94d24c6284e8a9584986341fccbc3f15877804ec45270c76f6ab9e4ceea6`  
		Last Modified: Tue, 10 Jun 2025 23:40:33 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04eff44ad16ec4eb71048095d27e51b0274d10fc24d0faab5b8a1ba2433741e`  
		Last Modified: Tue, 10 Jun 2025 23:40:34 GMT  
		Size: 4.3 MB (4299161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:944e013349826d38d096ee6960fd3e3b30527b62656c9fb6a3fb30400b20de9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cecaa25d08213acde5d79bca63b95609d80302f5dda226ddd00e080d1d83e0`

```dockerfile
```

-	Layers:
	-	`sha256:bc1f4b56dd34ea018454e05739d0dd2137e90e369de6048b67cdd871fb6a2ad5`  
		Last Modified: Wed, 11 Jun 2025 01:59:53 GMT  
		Size: 5.5 MB (5541322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0adf7cd3e6b6e4f181384e73b7466d0f18afbba2e112466c84d732982b26e013`  
		Last Modified: Wed, 11 Jun 2025 01:59:54 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d19ae5c4834399786534032dfa911ae14c3ea3ba94b941da7da35dc5e0b05ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50602075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c38c8a5a55c028aa6e2569591923e6346c3afeb2d68b65b94cb30bad3b04589`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49101641fdcb7c0ba8f71bd5a0f777918a056354221a3c6ec104096c54b7a5e9`  
		Last Modified: Wed, 11 Jun 2025 02:01:00 GMT  
		Size: 18.0 MB (18008093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb916921f0afa51e72645f6a7b9ed68d3b056276cf67a59c37bd7574f66b7ab`  
		Last Modified: Wed, 11 Jun 2025 00:10:18 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bc6bbd95daeacb0dcfde606b0fddf5723e506ec98ec6b2d3a8ad9bb8b8190c`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 4.5 MB (4512951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4a1962a3eae39004c5a69c7d2f19c249179864427ee83214c24e5cffffc14c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5565338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e83d10fdb1ab9f8d8ea67d82dba0fab9e627188c3d396f33605150745e85402`

```dockerfile
```

-	Layers:
	-	`sha256:13de2fc105385675bb4f5765f672e237f0310fcf7f004929a8204ec3ce1f8873`  
		Last Modified: Wed, 11 Jun 2025 01:59:59 GMT  
		Size: 5.5 MB (5546440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7bedde0ca58f57469b965ceac267db43ae666bda070664310630e2e8d3c779`  
		Last Modified: Wed, 11 Jun 2025 02:00:00 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:b37d52d9a1deab18f31456981789f369cbaf645970bc43e1c240e7618d84622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51582623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe0d2edd98e50fc4278a2320d403695105b83b6d76eb10446c1897cbb2468c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ce553daa5b6952eec3e672c7744b382f8050768eda58913aeeb063e3865c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:06 GMT  
		Size: 17.8 MB (17760093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b2f93f9d03254074cd5f6e732804229a1e44956262e834c5e410451f261c0`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfed092130dffbaebe5f93d077902971f6804e8878bd1c7d322be9516deca865`  
		Last Modified: Tue, 10 Jun 2025 23:28:05 GMT  
		Size: 4.6 MB (4606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7ab4630985df28324c6742da6f0fe77ad2d24322c36f06db691f7df6c6d48e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e802e841a21aab481906c270ca0d23ad4c538d42c3ad3db4a2dcbfefa232094`

```dockerfile
```

-	Layers:
	-	`sha256:f09338e12767b9027ae388aff3d27ea61e68e22d5567fbe02a9d41334040c671`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 5.5 MB (5536097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16bb974ef759bb85374f6ef0b4959cd65a7a2f47336dd442ae745fa0fb57043`  
		Last Modified: Wed, 11 Jun 2025 02:00:09 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:977e119718df50bbd19a36a5bbd66ad218ff3043fb6ac9e103d7110fccaffa4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49980478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb03769a57bdec1d3af0b5a9e488cf657bcde324ff50885b1b2c7097a9e5fc1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4e7372554ec27ec85d813713854d5262eaabbdb4dc32c8c7e56921a8eae86b`  
		Last Modified: Wed, 11 Jun 2025 01:12:24 GMT  
		Size: 16.9 MB (16905674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff12e1ec6727ed09e934c7295439183fc5286de0902c6cef9f11b2d9f49314`  
		Last Modified: Wed, 11 Jun 2025 00:26:37 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e03ed786872e05498eab7aaf02cf0270a30a0b974fb9da9ac3e641b53daf205`  
		Last Modified: Wed, 11 Jun 2025 00:26:45 GMT  
		Size: 4.6 MB (4554724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c770a8449598b27602779ae4f3d0164cfe9cad85cb912205190e0cd959b71869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b6abdfbfad5c99d1d61ad597a882ddaaf34932d327dc0c32baf097d9dc0175`

```dockerfile
```

-	Layers:
	-	`sha256:cc73a967f4705c4019848b099628330d8299fb0d2f0cfeeb18cb3ef69a675c4c`  
		Last Modified: Wed, 11 Jun 2025 02:00:14 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:c20fd3c9f2bf411ed5322d839de04168088410805c3c471f7232a5d0f1e4afcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55619922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a76bcec290036c73471af32678082a1cc365bfabbf0a46b67ab76e79495058`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6a520695abbed1fc01293696c3a22b603af508c2c5ed1a71733b79560eadcf`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 18.7 MB (18714788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c7d397e2cd771fabe0e4ac6683244a3a9d9e5f85ba9cb4f62c4202038fc778`  
		Last Modified: Tue, 10 Jun 2025 23:42:01 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b33bf8329fe58b376e60cfddc073f0062d265d9842495d7b1c927b55e15e4`  
		Last Modified: Tue, 10 Jun 2025 23:42:02 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:002c063c745ae7567254ed48d266760bbbc0d1b2881b38c20265cdeac5f9d530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509ac224886497da49a5d38deb68bb7e8868b87a6c68f357e18aa604d4a552a5`

```dockerfile
```

-	Layers:
	-	`sha256:1a72821ffb661c143c8f9f1df6836fda88b6b9131339c0099d8ad56a619d1c00`  
		Last Modified: Wed, 11 Jun 2025 02:00:18 GMT  
		Size: 5.5 MB (5547778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc24fa3c37b70f91b132b62f882b57ea6119a21e1ebed77f749bc8ea16fa898`  
		Last Modified: Wed, 11 Jun 2025 02:00:21 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:e5682db7a9f7bfec610e8ea3745e0d95042d0f90b45d5f1cc21f3997c99f962c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49671401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d726236873d9ab6beb3a67de1269e39d62c895d16256d6b20abdc49e074c84`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6e08090bd63341cde07cfcb415432bf680a6707f77daebec8e0ce6887e7243`  
		Last Modified: Tue, 10 Jun 2025 23:37:39 GMT  
		Size: 18.2 MB (18193546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f772f69d0914e0fc65ad8a0f591d9236a4b39960dfcfe3324c01f435e0f1`  
		Last Modified: Tue, 10 Jun 2025 23:37:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1bf22de9a351589cec379760cd62679723aa99be653054ccdccc94deabc95`  
		Last Modified: Tue, 10 Jun 2025 23:37:38 GMT  
		Size: 4.6 MB (4586648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:24b450c5297e500dc2f33da379ec72bac01c11c231ecd5e13f7c8fd49423b4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe130fb421769d90242e642daa59671e72ee88161d414ec5a277123cb668e628`

```dockerfile
```

-	Layers:
	-	`sha256:5a6f608e5f5cbbd248340aab576588c39549e420a1a95bdd3ece0450a0b02516`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 5.5 MB (5536266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a4088f467aeb478954db254a6c5ecd1e5df45ed7d85a6f44d417b4e6f3a30d`  
		Last Modified: Wed, 11 Jun 2025 02:00:27 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
