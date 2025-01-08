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
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.21`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.21`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.21`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.21`

```console
$ docker pull irssi@sha256:59bb2de70f7dbb1313bd140760a2ffa34af2449f4eca39978a3f232a51c9d664
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
$ docker pull irssi@sha256:1c3d022c5c4489c58313c68a812c32e4f08136554c2a6b94b3199c51c4dfbbe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19961270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94792a182cff39b869b9678d04451583cf1176cbd2390ba22d18040867099a2`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c5c15aad2d6db8199bbf63dbce6f5a287ca58a3efb2ef333a9d95cfd25eb4`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 10.4 MB (10380685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fc05c94cbd7efb358376daddef706181f2236a3981d44b28a7568aca194b06`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78e3622536a3fb099b94ef7c51d34b7160bcda9ad1ea9c2bfa2050258f41dfa`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 5.9 MB (5943369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3a2cffa2d8280ae57844e58006e1429ac6ab4fcbc6d09965417f3a11138a04aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605c489091254687433b640228ac33210f43bc7a1bbccbcaa39f8f3e00dbab99`

```dockerfile
```

-	Layers:
	-	`sha256:8d1d4bc3c4a5b1813ef80ac74a84a4b000c3fe47d02992aa3aef8a0e5036174c`  
		Last Modified: Tue, 07 Jan 2025 03:19:49 GMT  
		Size: 1.3 MB (1262534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d775116022ec28891b76aacd9ec167e1b1af42ff1f82134505edf5a906f62e5`  
		Last Modified: Tue, 07 Jan 2025 03:19:48 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:ee9cec0c1998fb6f18bcf9aa777a3ca533d0e42b30e8aedfd9d1e8018277b4ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18741050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a62180bf80df1815bd74d9a0c44000cf69ceea6c41542a5f016f32ea231f102`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armhf.tar.gz / # buildkit
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
	-	`sha256:31d4a7f5d4e2c1fd6b13116c69b324d9255a249ba92b63cd7d98924ec5438675`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 3.4 MB (3361034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1f69a329d7b147302b644c6f9668d44c13efe8dc5e6266ff772aec90187b8b`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 9.6 MB (9600816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c868b7f50c098a6304d16162be4a921188eaccd66b6343c4d81d2e3c94b1e5`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2845459a86a7126365b1a5367ee2f75ccdd95979d04009eae36320c59ec8b619`  
		Last Modified: Tue, 07 Jan 2025 03:57:56 GMT  
		Size: 5.8 MB (5778203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:ec4fdc5f27a6090b6016d3c47428c8245199352d9f018080818271c07b114ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1c49c3d2f762e9c8014821f537537dd6bd54397cf44bac2ed729023a191c38`

```dockerfile
```

-	Layers:
	-	`sha256:88e060009771210bde8a164288819ee0530155cf1f7ab7a5433c7aa3ab326a6f`  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:aff7edb9bb5ff2770d2cf9fb9d392ccb382e29d1c505dbf6215b38a27ef2b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18070006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befd7f754bcf61ff3fc9809bea4921cfe98ab48266419055a7b5a8ab614b9115`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-armv7.tar.gz / # buildkit
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
	-	`sha256:fa398bd1707194d783a6221bb60ba630f074222cdc0f4b6a05d9167d6e9c4a9f`  
		Size: 3.1 MB (3093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ebef5b655d5ef270a8e8458a29b96192d6b2ba2e34b940077fb41bb5641ad`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 9.4 MB (9435915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a192760c520e5cc5b5b3689d711486e868639beba801c1d7b6730bcd55132808`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b1e09a751940f418563830be3fe9cce7260cd91be5bfc06da34a2da7fb2a0`  
		Last Modified: Tue, 07 Jan 2025 03:42:38 GMT  
		Size: 5.5 MB (5539856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:3e59b96b836a868d4afe30f2d62a5aff6f906b39da31928875d8d14d4619469c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1283088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d4c6b0b665c3d2a7b3d3d016896c2a0b4b027553235a2d8dc7d122ff75a32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8fd89d1e3e45b9b1857c6b04c0a747e767839143415e85633c1c8132bc2a73`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 1.3 MB (1265415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f0cd5a29138bbb88e7c193e256c29662b9326e5a406f8bd9c80b9d5e6e771a`  
		Last Modified: Tue, 07 Jan 2025 03:42:37 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:691ae0906a101614add27dabdfd1fcc93822fe8e9d675db0408e8e51d6e97b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20149995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a074667dc577ae2e24ad802158944881b2ccc384c1c67cbe11e74dd0c9ad76fb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:707c94c90c597447ce10a36c9b56355c1cc67d0cf593a592daeb419d99a30d85`  
		Last Modified: Tue, 07 Jan 2025 03:02:50 GMT  
		Size: 4.0 MB (3983007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0e8107238dc99623382701edbc35b1dcb007686b241fb28bd982e7a82d886a`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 10.3 MB (10345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c3c121872d776d906ed119b1f9bf766dbc3bfdd25ba8c7cf796faad3f2ac95`  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4da9fd1d1181a4f7d82ed0539e4d9960e7838d44a3f139e19a2e173d72f6e`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 5.8 MB (5820970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:59c42a21dffe25b8f8005f39c8e423de7d3a540dd9534a20de24ffbc9ee654b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1280363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53eb10127998742a31fcce4c30f83db84f9b737e4d565f96c3ebfdb94dffa620`

```dockerfile
```

-	Layers:
	-	`sha256:bae129cad212dd7519c944a8d167c74420421139e202915d62aeba89eaf97104`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 1.3 MB (1262638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b168ba964b60aeb160424e0d6b2df91a7c9334855d272f1556317cc813f0671`  
		Last Modified: Tue, 07 Jan 2025 04:17:13 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:505a31245cdcbd957ed985b9799487ef025c2f0f1a065831804c638035e45ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19425605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffa412b3b9796f36b25807e221eb7492add081b914aa3ec5a9a6de296e733d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
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
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312d09aa529ba7d13f48735b67a19ca729c9cd44190cc4498048b1fc011a0647`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 9.9 MB (9934127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dd68bb5ca29c8e8825109475ac0f76aa960a608cf516b8d99ae157fa413d85`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ffa286ed7164235fb4a5b5060e02de2b963da219ef763b487f10ba409f2ef`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 6.0 MB (6032213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:127eaec9b140c6ad52294a8949930d6bff9916ddb728037b6d7166f4dc82717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1279972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd126088b6191982261984133cb4ce4462f8083d4f82414b2748c2b8defa7a8`

```dockerfile
```

-	Layers:
	-	`sha256:406f69c71b22a64416f63fbafdd8e365e1e6280e9e634a5ae489a5d0efe20286`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 1.3 MB (1262489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec70bb265709a071b70e4a8eb0596758310d38afa7ca089ec7f342a8f3051811`  
		Last Modified: Tue, 07 Jan 2025 03:18:09 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e1a07191b985066901949b751abbc3a8705399a86025070a1b8d038bbc03e25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20355103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043a7c56807b175fd4ab43167538bea09d3165d9b0d915f029f2a921336ba5e9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984430d20ca5a12c58a794cd6735eb912905d5e61cd3118245bbed091db443c8`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 10.6 MB (10581065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebde967f7f27bbcc4394cd1b4ac0c83f2385f775899d4b8ccf4c9cc643b3b57`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa409aad1e8a4794aa9c081cc0bad837f66656a9a638acbeafdc81663342142d`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 6.2 MB (6205301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa0e7cf0bc9f1b4359a243d0dd54a64ab1a24e8ea6485ee8940127e20e65926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddecb51c4676ac3edc4f245f17b84c2b4935079ca376356f507160c3bfb8a24d`

```dockerfile
```

-	Layers:
	-	`sha256:6ac7b259ba6e04b659da190a53bc2e477483a94bb56cddf9b721bf212a3ce6c2`  
		Last Modified: Tue, 07 Jan 2025 03:47:25 GMT  
		Size: 1.3 MB (1260641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9830ae89824eda0433c75d1cf33099e8cb27383d4ebdc34b39d45f8e37d013a6`  
		Last Modified: Tue, 07 Jan 2025 03:47:24 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:d38c24242d7dac0fdcfe2abd105d22b58215651c186b5d693800d11994032f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19128766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b045edae0c5bf6193ff39c5a48b65467c8ab2a3c96714f1848a7a3874172523b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:7ac47ecf3caf977bc5a9f6efe0249994a504165670ebb9b6fe2c478617c5482f`  
		Last Modified: Tue, 07 Jan 2025 02:32:47 GMT  
		Size: 3.3 MB (3345140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56c288928e98f62c233767dbd87fead8f85b26967fc7b5965719de2afe61fff`  
		Last Modified: Tue, 07 Jan 2025 06:34:10 GMT  
		Size: 9.8 MB (9825934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17280d72810612ad2508369db46643e1375642b80877bcab2668c371b0d4b20e`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481769b90f80698d41e9f82b7a677058c0b76f557c52074d0c2b2d1e517b7c20`  
		Last Modified: Tue, 07 Jan 2025 06:34:09 GMT  
		Size: 6.0 MB (5956698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c16dcbe172508e3381e8f129eef9662e9319b5340ed40eadb92ad09bc15d3318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd5a5355396ea2bd811f677c5cf1f08de5ebb3131f183829ceadb45f2b13010`

```dockerfile
```

-	Layers:
	-	`sha256:f5a3e9eb1c5eb0407efd87ad4c6a4cd5f283ba8a82fa68f89cc12e24abce3f2d`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 1.3 MB (1260637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e3dcf950a4626d17b25d7f600ff023d83129e98de6d25f9a53a5bfd520ff680`  
		Last Modified: Tue, 07 Jan 2025 06:34:08 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:1ec36934a67d8702bb557a938447714a859ef6a0cc9147dc8355cef0378ffb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20502981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446dd276662f87f1c1c700e53a91ff680dad84add64f4305cb017632f99586f9`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
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
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e15af58f4423c8012c8a197ee68dc0b4fdc4fbee3327e28a99e7797e5bff95`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 10.9 MB (10943065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2618628526848743cfff9f813ac77cfbbc16319c11ae7af0f22caf8d8fc4da88`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f879587303f200e4a204e19f85d09f85c7be0a0a6833f62ed458ebb6c947c`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 6.1 MB (6099471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:80f71ffef49632ebcaf6dd8239eb3eaced12f1d1f0630f9909d3ac0236605b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1278126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97dc26e3a3ffd46eea62ff534222770e11acc833d116fa37f5c47dc9131ec91`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8d06c8901e95fdd2a9e2cae09c6968cc5f6eb790de3b4c7320c54207755ce`  
		Last Modified: Tue, 07 Jan 2025 03:41:46 GMT  
		Size: 1.3 MB (1260583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d310374017961e3c420c1b4b193cb3f019a8253b5041be30194fdc6b232beaa1`  
		Last Modified: Tue, 07 Jan 2025 03:41:45 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:8a4aeaa708a1996e7b424b62ba33f2339b2044c51c8f64cfa1380d533b35f4b4
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
$ docker pull irssi@sha256:23057ab212e9d15a741412ee964f2cb4f0f3985c118be268624a009a89a0d754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50905624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344997ed817a8c0519aec3fbc68034b1d773ada04d275868e62b1b6ab04d5ad6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c72424751c946aad602294c0df5d40037ca42682cebec04a4f041ee2be9e87`  
		Last Modified: Tue, 24 Dec 2024 22:17:33 GMT  
		Size: 18.1 MB (18077911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87dc8ccdaeb7bbf6a9e9254d58992f7fd7f7182215f7405a0fc365c70f8f5be`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a51446ed8c2905e807f861c969e3a41d073b88ba6eef4fb16fd67bf3de189`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 4.6 MB (4592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d8645bd2d7f96a8dddad326c5143053dfd95ea0b89e52905f5a3749245f7a07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b697f83abdc916ef04820de44bf1e623c537cd8341361e3cdc46132c5e5d81`

```dockerfile
```

-	Layers:
	-	`sha256:61398e9cd51cd66cb2e99f591f2b9fb386d4695d4de05bef16f192121bf03fe2`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 5.4 MB (5378443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d928a21e7945ff14be8f994621ee799b35e23a723350e66d943c2cf3c4d0f3ee`  
		Last Modified: Tue, 24 Dec 2024 22:17:32 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eadcff7b70e8912a3dc50df6d0e44b26e55b242a1581480011d0cf8fb4b38885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47048818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e14c37489453fbbf90d3852633d98161aab72ce3aa81454880315580510c268`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61230a432de02dc9fd57340d88179517d7f651caeb2a5e2fa6ec333d17ed65c5`  
		Last Modified: Tue, 24 Dec 2024 21:33:31 GMT  
		Size: 25.8 MB (25754907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d756fac1c4e135e181b6e10f08354f7a7a02217168b7c78249436b2c82497dd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 16.8 MB (16845985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154d60a6ca7c1bc777138f132a9f61cb69e9d8f66e1264ee9c10057f4b60f876`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b0e73b2f9262b2d7596129fa036087da462b96dd4eac08db8c2bfc7dbbecd`  
		Last Modified: Tue, 24 Dec 2024 22:33:40 GMT  
		Size: 4.4 MB (4444570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:62280ea2c112e6c4583d51eed89fd101f3c22ed3abda1562d6abdf86c22ec353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7da0feda91bdd37225cdba44b95ca9c5ee721136ee45fca28e6234474750ed`

```dockerfile
```

-	Layers:
	-	`sha256:c5dcc12577084f8eb24d9bc48ebb8ff347d05beb9b3641f975830cd05a9e8469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 5.4 MB (5380052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bfa1c188916b411bdb9ec5a20bac6afafb191f716cd1585687545fb1d91469`  
		Last Modified: Tue, 24 Dec 2024 22:33:39 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c60c586195c1b6d831d765db2aaebedaa23f5cd8c89031bc29051de75b392d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44676740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840a0563ebc19448639806f7bb6d88e47ee9fa863e5d66af71635306096ccc8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac2d76558b26c2d29bd3b0d661434d6173ad0255ac357bc1b0eb936df877ed5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 16.4 MB (16440781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ca7b68fdc50a96605b21e2ff74ab5ac4b8642875034c13be11472cd962098`  
		Last Modified: Tue, 24 Dec 2024 22:32:37 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba47e1eab4f52f16a0ebf6cde2a2a0c0624c37afa514038f8aa4bddcdd82bee5`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 4.3 MB (4299083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:537f4343b468b13181de2ae031bd16002f2f93b1f3002b2fcb27d2d3df0bb0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88117b9d7c5dd4d4f4d630cf8389fc9cfab8fffc2ce4d6a3e3a3d27025f89cd`

```dockerfile
```

-	Layers:
	-	`sha256:3e326db06a200c7054291876c43280cc704dc20d413c080346d8839c37204fcd`  
		Last Modified: Tue, 24 Dec 2024 22:32:38 GMT  
		Size: 5.4 MB (5379801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e12aa5aaf85a263b7d5ab5c79f027744ceb6eab3a345d3cb1c9cb9bb8a955a3`  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:67ba6c50eaecd970fed89e515567e5775d695bb6c8595fd8eb0bbb382c941403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50430209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d066c64254f69dcfbf7fbdbb04466926dad75305a2e30cdc44556bd73fcc3580`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5defed4f387a259c12dd6aba6a55bcca5f12528d9dc98d56e1788e39b32cdc11`  
		Last Modified: Tue, 24 Dec 2024 22:54:19 GMT  
		Size: 17.9 MB (17855086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accc204fceaaba7801bf27e6a416f65a7ba7588c33a04b53a1a8620df94addc3`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59452d743e2018a043d72664977a6ed9cfc55da0b0018177afc6930cc7207474`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 4.5 MB (4513045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:891dca0a83a3cbe6caae3736c2b8b8d4ae478bbca3cb103abf832033719499e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c474e1fc07df6f654a4a71f6c0165a8a9c2c7320abb0184864faf354d0be836`

```dockerfile
```

-	Layers:
	-	`sha256:b00f4ec4af66f492dafd182b0094e8f6fc59f9c4d6f3de2ef8797f83821784e4`  
		Last Modified: Tue, 24 Dec 2024 22:54:18 GMT  
		Size: 5.4 MB (5384919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3afee7b7d0daadba8ed43e12739820878f1df08b9d3eab75e57a6f1c9270fd35`  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:8101996dc9479553a158deab1ee69af3df0fadc08bf5cee3ddd1f9b238970753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51427239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29b6d856e663d8467ef6d90737558bd8ebed0a59d68453dd3f36fe22a5742c6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0e21ec2cd7bb2aff9e70cde4cc9bbc54d02b13d6930570ff1ecf4a9ae95963`  
		Last Modified: Tue, 24 Dec 2024 22:14:42 GMT  
		Size: 17.6 MB (17611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c47df341479281275b707e735f4cdc8ebef6c46183a535af20044dcf6e1cb6`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e44ee7c0c97ca47f93e7daf7e5407163e40a64d218344a596b80dc17576c`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 4.6 MB (4606587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e55141ecad773077ba5f08912a8c58f0896a2e1430c7a272361e077c06ffd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff42324626ede8be2da9b0b74db7ca020d72089ecffbd7e45916aeb0f0c9ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f085ef33c3d223790f6b552859a2bc48a5de2aa56c0bc1937006e030884db471`  
		Last Modified: Tue, 24 Dec 2024 22:14:41 GMT  
		Size: 5.4 MB (5374522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5acfc46e05bd06262f5052dc8d142bc8bfad9e58427b545f0a7490ce7c84d6ae`  
		Last Modified: Tue, 24 Dec 2024 22:14:40 GMT  
		Size: 18.7 KB (18659 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:718af1da749b349ffa56de2c97509314842942b1ddc45425a962589a8fd1d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49820506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda2c4510f60cdb159440834d8967c213fbbe9cb1cf65d61dd165d6338ee9ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d741c8289452010c3aa785f22f08a467068eee35fff03ea036195dffd4f0446`  
		Last Modified: Tue, 24 Dec 2024 23:11:15 GMT  
		Size: 16.8 MB (16756416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48873180dc87eef17535e51e50b0437e98545a35b83e65c242629e484b35c2b`  
		Last Modified: Tue, 24 Dec 2024 23:11:13 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169def72d088be85942f65cc354e6952896ef71a9e0ae829d567de7ef7a3cff3`  
		Size: 4.6 MB (4554865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:78d53b6acb9261a97ce9360a4be4124dfac0a969c8cc49d154350a423d4d4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5c5bd040940e4f52e32cf65f249b45878eab2d310a41ef29a47a6034f09d77`

```dockerfile
```

-	Layers:
	-	`sha256:09652849ef767c4aa50a1db1cb80f817aaa41c466de58fb5a9c0844bef71dcb9`  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:368ca1d80560e08559ef9d644097a754bfa6615e345ae367196597d961467934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55480816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b954e361680b982fdb593f47feeabb7866377ff980408199906de8c4b62e78d3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf30d6f351b66cd9b6d1560ee9fbb2792ef6a2dac398f3d5bbecbe1bec5fbb`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 18.6 MB (18585472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4426abb9601636cb08c2051d18318d3dc52d6bc7d66a2031a821dad55a0447`  
		Last Modified: Wed, 25 Dec 2024 04:09:30 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29088cea4c85b9221b1628d1c9f344a9a488969df69a8f7884ec384e6806d92d`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 4.8 MB (4828748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:cd600a34bd1bd6b122e3d9d85378a5f438bb223ac0e58e6eb07953c1de5749c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5404925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37695e9aa1a47bdd6deaabe5dc36ae13d8fe8d722cbc7503875b5083dc42cb4`

```dockerfile
```

-	Layers:
	-	`sha256:e718cb6dd88a3ae3252d2f7377faa2502bd81df1ddfb4fd59526490d940e64db`  
		Last Modified: Wed, 25 Dec 2024 04:09:31 GMT  
		Size: 5.4 MB (5386137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90976fef992efe03034f56638b72783d85588e0ce95ea473a07652dc3ccf5854`  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:6d4f8c86591f7f099005f603c581519898916629795e016f0ad6c50c54c7e358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49506570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bf4610803dcd64fa9c1a18dc7160f295697d8183b5288aa06d304b2e66426f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5393b1a641f2765ce0615f8fe15377fde13c41dfd16d1c961cf7aa4fd8afa7`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 18.0 MB (18037644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803e78d7184cd114dbe79be927c3e3506855c70dea9a4f3d39c3e4538a599c8`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf411f6cbc64f23f43e2e003b2f5548855b1dad9b652e60fb7e7d101afec70ce`  
		Last Modified: Tue, 24 Dec 2024 22:32:32 GMT  
		Size: 4.6 MB (4586671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:b4883624e3e145f715a5b97c7f8eb695a1eefc5e5c5ed84e2ec227b4bfa8e3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e5a4d4c916759088abf1effe5a96bfb1297463f9bc907796eb53d063df3bc`

```dockerfile
```

-	Layers:
	-	`sha256:355dd2eb2993403778fb62fbcfaf811ec299da468b29a24d4dbe76418719ea53`  
		Last Modified: Tue, 24 Dec 2024 22:32:31 GMT  
		Size: 5.4 MB (5377637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098bec0f221c0eb040d65c5ef3880f74e5ca67fe2080b983160bd0154df22f3d`  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
