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
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:56 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Fri, 30 May 2025 22:57:55 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
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
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
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
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
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
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
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
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:970ccc9dce483f6c1440d67e7c467cd7417a8be5caff7ae283173ff4c640ed9c
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
$ docker pull irssi@sha256:7dacee79a4139ef220b0d44a4021cf84d86cbfcfd7bf173f02a2e82e7a0a4f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ccf5d5ab5413c8968a4f4348bf2a8cc8fc1e8f99459a195eca5531ada4c064`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9b6bb1bcc6ae843d49f69b0e3ca4dade137a8a8557a1db4deff5f8e0da3c1`  
		Last Modified: Tue, 03 Jun 2025 14:24:08 GMT  
		Size: 18.2 MB (18230579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9ae78eb5ecf43b16884dde4e2fd2ab35421091a2d683f87946da57945f6d8`  
		Last Modified: Tue, 03 Jun 2025 14:24:05 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7cb72d3de1e1a75057ce9293333431069199ae5f45f2c1b02e76966ef0ea80`  
		Last Modified: Tue, 03 Jun 2025 14:24:06 GMT  
		Size: 4.6 MB (4592824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9c5998e2fb076b708b367cbcdd14293b98a88bf72024befbb2d1f1bdf1f2939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5418342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591e2fa7fc6f5c5414c715b248b7b46641162c77a6676dac9c2ca9590bcfadb`

```dockerfile
```

-	Layers:
	-	`sha256:5a1a20100450a1f230355c2304b3bf0c0bbf9ac38b6b046cc1c22c22cb9d8dd7`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 5.4 MB (5399626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0278efefe3d25f15885a6b685bb55d9b86d43ee7b8f8469df0d8bd4eb5a968c`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:fad19e6c7e0c478a464b5c78a6267d165e17c1e9aa1c5554fc55b8b6805904e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47218909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea45bbbc7d2b57e2b4b93345bf5a0ba8c28454989eef047126ab8b2542a60a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6caf5a49cb5d4b9aa5715ae76ce980c6cb2f72ebf45a019967a4ea9b751844b`  
		Last Modified: Wed, 21 May 2025 23:23:57 GMT  
		Size: 17.0 MB (17013939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0414e7f328d514fd6a026827dcfb678c4b74a4a85e20b60582a1a9c2d0f29df`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b96b0f7e078ba13f219bd1cb6fd31c23335a43ea694857f79ec3fa4fdee9cfd`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 4.4 MB (4444716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d350d28935b5c37b9bdfb70e6b7c5bcbc0d409587521db1cbdec9bd4e109838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a927b843d501630270ed04f5b921aaadcd48283dd1f95cb22e41aba8aa4e314f`

```dockerfile
```

-	Layers:
	-	`sha256:f88fa0855358d75c2089bcefa9e285cb818c58a04bc3138b8436569f8df7d328`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 5.4 MB (5401543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3910af41e64cb730e2e0d59d748b22cb4da0706fac9fae8bf7bc5464b8057260`  
		Last Modified: Wed, 21 May 2025 23:23:56 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:f42a682d45ad40f5fc8cdc7e39ac1ee4221fb59be170856babad5a59b778cd68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44837653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afce4e9d4a3905057718406726756d113575a8607e9f9cbcb2956e30f77bcbe`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c880bb0b1caf3f53f220e6cebe552f499ad35a277492151d9fff8abff399a`  
		Last Modified: Wed, 21 May 2025 23:28:10 GMT  
		Size: 16.6 MB (16602256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fbb9f342faeb55d0be5644f180d2a5bfecd0013e04ba50f50d2aac4780f492`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0f3a125243a7c0b64e2ac41e10c3878aae3a87031a485e8db8be16fee90d3c`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 4.3 MB (4299121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9a74109f8b81a93ad24fa407cd75b59ddf2aa7d6045555fa4ca20346445ba939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd063dc9bb97507aa8fe20459086339c2d769d8d3e8707f261a60f05b1852534`

```dockerfile
```

-	Layers:
	-	`sha256:15ed04df565ae9c5214453d5f6069d338ccce507ada7e041b1ebb972b1fc590f`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 5.4 MB (5400984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfcd59311e2cb43a9ce60e79bcd29bf4f2548b73f0177249e1fcaa4c24d688c3`  
		Last Modified: Wed, 21 May 2025 23:28:09 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:5cf20aca8c5ce61a43c8c5a2ed782294d80d4bd3c9c48e903d53a93d03f019cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78207a045785e020b678247dc4ab32f7c2049a1e35e5e30c3ae274af9c99b809`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d20f8d1ae505e800b360adc71a68371c39b10a1443678cdcb1f66f23e382d6`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 18.0 MB (18008669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6befb885e0c998923d9514b4d3452b71b1e67801a9ca8ba4caad2be77cdba`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be631d93cbd5771518099863c66e8939ebcfeccbed7a18b4b8306195b02db05`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 4.5 MB (4512954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:3b5e27ef72f0e8244542794eda3d15094309eb188e60943999c7a4ace5eb5f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5425000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca9025518e4089dafca279da0c018d8ab47b488e88698afd96dd0b5b0ff3a`

```dockerfile
```

-	Layers:
	-	`sha256:bc0016bcce372a81f6c919d75b273c7153cda962521c7ef3024fe087612ed13f`  
		Last Modified: Wed, 21 May 2025 23:59:33 GMT  
		Size: 5.4 MB (5406102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b94d19a32e8a4c2c8e1156f42a26ae3e0baabbc64ea99cfa7fedd2735acd8eb`  
		Last Modified: Wed, 21 May 2025 23:59:32 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:ff1e71758035ab4f304d61d31d2801aed0e74262e5c0999fe163df0d8123a52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51577420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a41956090434c9c2bb0b3e1aac490308a22d07c305741da019169d10bf8c08`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4500c5b6bbdbb1cdad6533fd26274c32e2751bd21372f3002bfcf9d4e8ee5d0`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 17.8 MB (17759944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fcd66bf013564f09a7519c8514ddc86ce701b76d0475b6259173657964782e`  
		Last Modified: Wed, 21 May 2025 23:12:52 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f217b575ecf4ca0ece105291e2b8acca516528d37e2605efa30ee7e7ef2a53`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 4.6 MB (4606634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5e1af783b963d1762c536ce4b313bbe2ecd207d69ac8aecfbd7b4a0a95e1149e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6743013bd0fdf44b4b5f367da215b302129fac8ccb8aa3e0fc8d35d0fc89e5be`

```dockerfile
```

-	Layers:
	-	`sha256:430442cc858eda2508e15cb90017275bd617078eee857e0a6f7803a4a4d48827`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 5.4 MB (5395759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7beab2b1ba82e953244100c7fb5ef0cdbd8fc474bb9a153ac68dffec0d27e8`  
		Last Modified: Wed, 21 May 2025 23:12:53 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:9716d7cc0813e81f08c10831363bb53be98b6a3b5440d2781a7cd6e3fdb56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c83a7b9534a9888e48586e43a94caee9781315e0938105ff37709981babbb93`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d99f66e7b1765c3ec361058e6a430819f7fc30c36ee092ea2edbe758501b6c1`  
		Last Modified: Thu, 22 May 2025 00:02:24 GMT  
		Size: 16.9 MB (16905886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061a4dc2ac39aa73de2009ef23772de195167ed98c1daf1b7b6456e70b1a55b`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39abf9b39574c1a47c801a3a5925b542d829867ee2498e4167710f7630d2d11`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 4.6 MB (4554826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:703a5bd8daa2140d4dabecb122834b6e538e551d4d6f692498c073cf810ffff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc98f752ff82f7242a31b49831e2064694f06ab8d2699a1429b217d81f68930a`

```dockerfile
```

-	Layers:
	-	`sha256:5dde94c34894e9304076a46d08dd97b57613be02f761e3b97a2021d2f769d6d0`  
		Last Modified: Thu, 22 May 2025 00:02:23 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:d39c6c4a484070438f76e4d2a5daf17a512594098e06fa3d7b4238884be44359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55614303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538b743ffbbf4eb4da4fce8c06f0ff5be617a8b309a81dce43b03ba527092041`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99219dddf8ec63e97b3c3e181cb033c2eb73f2e7bdd5331da92dff17f290026`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 18.7 MB (18714945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f82e753728e391bf662e3da5122225045da9df30295352455634436f15d4f4`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1b163d3fdae6637bbb37f6cc8b65e2d6b91df7bbc9306e4b2f0a94d1e05ab`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 4.8 MB (4829089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2af7fcd95ccafa7a3c7cc1992d13a1dc954a13837294e38ac44db86a55cb7e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421a09f61cbcbf3c2f19b15087abe0a12efb2a941a57efcb4d151a9a7a31e9d`

```dockerfile
```

-	Layers:
	-	`sha256:11fe7a445b09dd8ecf06108dae3cba6b71a1f0a903fe077b5e2b3158818a16cd`  
		Last Modified: Wed, 21 May 2025 23:29:51 GMT  
		Size: 5.4 MB (5407440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58962c2621821c7b831ae452e740b123affe038337eb43ef2853991c34d4e0e6`  
		Last Modified: Wed, 21 May 2025 23:29:50 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:c8595cf22300c91ffa7c488004078d84b23575b4218ff986bc985f397b396256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49666464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd9361db529645acb42954cc6532ccb26ed31140f1f89be684fe18309339bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1697f0ab27e73da1375593fbadbadb14bca1b2837d5d9bd9c75b4eacc66919`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.2 MB (18193563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa70775cd05129ac62866dbca843b61ec92afdb706425aa264bdc397456d593`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d0f46d0539d8a2fbc96f7b744dd81011e2226c396cce6d0905c07fa108b64d`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 4.6 MB (4586738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f53e7c28e86172300d3a812ed868c5a8742954a807e239579a831252d4c00f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5417536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c66caca49c20db59cb57cfa7e0c83f223a485c55a33a87dff4b666ebc9c414f`

```dockerfile
```

-	Layers:
	-	`sha256:cf218f333e8a2b4f81f22f34bf095c567199d274161470c57bbb7c0ae4258c4b`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 5.4 MB (5398820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c62e336314491e1692c32facb8d905fb78fc36e5936f9a1ad8a266658dbdbae`  
		Last Modified: Wed, 21 May 2025 23:23:59 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
