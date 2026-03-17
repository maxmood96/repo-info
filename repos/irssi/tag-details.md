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
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
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
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
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
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
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
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
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
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:cbf9e0466eacacbd27eed4758f8917f4345dfff561d74dae2a884386186e3279
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
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
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
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json
