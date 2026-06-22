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
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.23`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.23`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-trixie`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.23`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-trixie`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.23`

```console
$ docker pull irssi@sha256:c65b1f7f4fd1943ddc6209937f2f5b00a80298b224032f50e475267a7c3c86c5
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
$ docker pull irssi@sha256:ee97c76564b57e4bb7e9095822fc55b75297ea61cb745181d626152385c4600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20725683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004acb4b5256aa50ff297f7fe6c7b2e17fb73ed7d050f72c66c1d05cf5beb121`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:14 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:14 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:14 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:27 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:27 GMT
USER user
# Mon, 22 Jun 2026 19:46:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1e94f1984d1a34781222d067c9e0fb4246ed50ba11ac34de4f8546f4e2485`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.8 MB (10817260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8ebfd85bd55d38847eb7338e5e45eb39412dfab6fc7f745757724d626fd08`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28df43b22dfc13f2366edbda7491c5d8fbdfa40ee29cefdc6d4e9bc7c4fa74e`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 6.1 MB (6063016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:520d0b373d64902a539d204abd3a42f4c7b273132959ae3590994f6d2dcf8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5a09b1ad68a809735a39bcd0a8fddfc609a134767d3364ae7df9d8fd58b296`

```dockerfile
```

-	Layers:
	-	`sha256:5acaec97be559a688326f497f478dbdb6e4915d006b76c4b53e8bdd64088536a`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 1.3 MB (1289892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7af272cbe9b3c649aee4fadbdb5505dd378ef44316d06299aad532db0f1c5cf4`  
		Last Modified: Mon, 22 Jun 2026 19:46:34 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v6

```console
$ docker pull irssi@sha256:0e3aa1699cea3307fe17198c9d1cb8fb606f07392b9ee525d46dd49235f9043b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19470670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca66492574e94e99685d079fbfebf446df2347a5c072b0fc173cdaed678b068b`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:01 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:17 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:17 GMT
USER user
# Mon, 22 Jun 2026 19:46:17 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82defeaa7caa2c7d4266000dda4c830bea74f161848ccd918a9d75c9c85b18e3`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 10.0 MB (10025025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7063e8d3be6cd1169a61752e1d98a649d42f3c0931936a2d787fddcdebcdfe79`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977d3156c4ca4aae124c90d37aec9ee6375975089e18395cef1bc87aa6d6ffc4`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 5.9 MB (5892065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:d3bfc6587b61a29b57468e9f85dfe1f0185277328cce7eba62a7a0fd9807b1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ceef14e9dd6f7c90a99f80faaba2298c95552c1b00a056bff999d5659f141a`

```dockerfile
```

-	Layers:
	-	`sha256:d3172774ae94b48c3226b7e5176879db7e72a4d4d97ef5c1afcaa5b6820b2aac`  
		Last Modified: Mon, 22 Jun 2026 19:46:23 GMT  
		Size: 17.4 KB (17423 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm variant v7

```console
$ docker pull irssi@sha256:c6346492ffddac8ad99270069266d14602d3b16426778772b73406545faec005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18765246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90939a86a350a9919fa3e8972b151397d7b54b03ee21435ee544bbf677a0f09`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:46 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:54:46 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:54:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:46 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:55:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:55:05 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:55:05 GMT
USER user
# Mon, 22 Jun 2026 19:55:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea6ba6c89e64b810b05f4345c90018d99187b4908ba7c678fb2da59ad298063`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 9.9 MB (9858991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73405b9e5926e564109dbcc12631ae70b008dae146e7574c6d6d9942e4a808cf`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4db8da01a044ba53423d803b4956366017b1e0857313b152eeb27ec164280d`  
		Last Modified: Mon, 22 Jun 2026 19:55:13 GMT  
		Size: 5.6 MB (5643416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:465fdca29637831598f18eb6b247ab253e3198e3dd41df98a04ecf910d7499f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1309934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fabaced20896c96987546a9f128e97a46f75331be1f133a9ee80bf5ee699d6`

```dockerfile
```

-	Layers:
	-	`sha256:83c2f3976ccc4b3f7141e2000c6b6ff5368d5afee6ce2302d029033297cd996a`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 1.3 MB (1292300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e9f8dde6c52979c4e2eaf369d9a5677dc407347f63fe392c1c609c8efc15ae9`  
		Last Modified: Mon, 22 Jun 2026 19:55:12 GMT  
		Size: 17.6 KB (17634 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9dc603beb4a07d393530d95086db6dddc1a1534d7d09a221a326b0bba478f895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20869826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a734a9b36fa9c8fafec921fed6ef5a7913568dfa78db72a7c40c353190ffdb5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:47:01 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:47:02 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:47:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:47:02 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:47:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:47:13 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:47:13 GMT
USER user
# Mon, 22 Jun 2026 19:47:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1314d0c4d705abd2003b834ff222929aadee219573406905b1ebdbcb2fd0e5`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 10.8 MB (10751011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b51ac442374423225d78f343355d2d1c4916b10252075e88ca9413f5e1431ef`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b41dac8613012dcbc45b580ab5d15c02974c28e2033d81a371533dbbc0b2f`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 5.9 MB (5935970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2a6f14a09840b9202c0cbc299b854b79f25cded499de1d99f9663655e47c68a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15c812595b215a1aeb63653f112b73ec5a48ba4b63fddf376c00305bb6c0efb`

```dockerfile
```

-	Layers:
	-	`sha256:3de740e24bda3370e066e00f280a3ca5156edc7f363250326e7ca0c5100051d8`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 1.3 MB (1289346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff8fa68c15d34a1c878b54527440ce7ab0b9ceb6a9d42e821cff31d2e91afad`  
		Last Modified: Mon, 22 Jun 2026 19:47:20 GMT  
		Size: 17.7 KB (17681 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; 386

```console
$ docker pull irssi@sha256:bff44ff5f28c28096901bee2b6a903a831bd237248e35f57bd5b6320cda08bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20163548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e40dae22529a380af2f2d1dd3100c569877d7ba9c4b1051e64df9e52c88e87`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:08 GMT
ADD alpine-minirootfs-3.23.5-x86.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:08 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:11 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:11 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:11 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:28 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:28 GMT
USER user
# Mon, 22 Jun 2026 19:46:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:732d51f3795f48d3898f2f5895e6c5a28a5feea9889892adc95157ed714ca693`  
		Last Modified: Mon, 22 Jun 2026 12:03:32 GMT  
		Size: 3.7 MB (3667990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1630aba8794abec3af226b1736b6b62797443e3c4b03af5bf02dc67b2bf22a7`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 10.4 MB (10351196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004e325c3306131ecbe3ef3ed32a950855cf6b711aad5296a4b6936c462f7a44`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1525ce92cde60047ef81b57e8b939c9ee067189240d2aeb62bbca9c118800fe6`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 6.1 MB (6143379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:2ae352e0f4ddcfa3cbcae809a0abe748c999bffed183bf538d88fe9d59d60143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1307291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a425fa3680d2c2984c776bc56be97be44fbbe15ceadb3b71c923e02708aa04e`

```dockerfile
```

-	Layers:
	-	`sha256:2b7236139a451e3522be5b28e2e5f07dd6135f951dc3a7cfbc38053c6fa2c51e`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 1.3 MB (1289847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ccbf6ecb50a4018210ae5bed44dbd5932652fbb0f487e2f755fb24006dfef35`  
		Last Modified: Mon, 22 Jun 2026 19:46:35 GMT  
		Size: 17.4 KB (17444 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; ppc64le

```console
$ docker pull irssi@sha256:36bd8f1c85c53276584b31ecbd4fc8f2290a8f8aaa4758e0e4070328367a8cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21215327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fd75983e50e468a396b0ec585adc7593d3b79eccd40d17ea6c8616aa3dedcc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:52:59 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:52:59 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:52:59 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:52:59 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:53:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:53:20 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:53:20 GMT
USER user
# Mon, 22 Jun 2026 19:53:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ca1493cc77dfa723bed221766a958a4b6713fd5cbe7323645d82dc22d9eb14`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 11.0 MB (11039519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efadd163d0d496a592324d86ce4b1b0d7ba3a6162be35fb2ca9ad34b1e410eee`  
		Last Modified: Mon, 22 Jun 2026 19:53:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ce0cfe8881f2132dda000a5eddabb0994150b10fda5290e0fef5771c18393b`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 6.4 MB (6362524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:09a17eb571ca45406713a69853c7bdc6e2a2a892ceb44c9ad5f9ea60fb7504ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686b4270754ba7801cc14fdd9985f93980a39b76edcac849924bc4d4b990b87e`

```dockerfile
```

-	Layers:
	-	`sha256:b93f61a4f08643a442eba6357584db91c0f8d3c58b0e57c1924c796ccfd7ad1d`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 1.3 MB (1289299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a082bb19995633572b61251e374f85a1aaaf35209d26bee8c85bc2bf6d9d6ca`  
		Last Modified: Mon, 22 Jun 2026 19:53:37 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; riscv64

```console
$ docker pull irssi@sha256:94b120e9b15f5c81091f116f5e6e5f913a8cb318cdd41eb40e22b64946655446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19885865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d505a244fb87c10f37d80d6b2572243b3a37083e45fed0a3c289a67e5a552da`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:30:17 GMT
ADD alpine-minirootfs-3.23.5-riscv64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:30:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 21:02:34 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 21:02:34 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 21:02:34 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 21:02:34 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 21:06:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 21:06:24 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 21:06:24 GMT
USER user
# Mon, 22 Jun 2026 21:06:24 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e5860a6401101356d3688f519ef896539fceeb0e505b24a7224fe7e76fdb1`  
		Last Modified: Mon, 22 Jun 2026 19:30:41 GMT  
		Size: 3.6 MB (3573240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f730c254988ca0282bd88a0dcf04e16c9110ea8c311d08a54205ee9be1e6349`  
		Last Modified: Mon, 22 Jun 2026 21:07:19 GMT  
		Size: 10.2 MB (10248751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa85364964156e8bc871a2b1ce7a6933a1fb636df5f26523b8daa2fd22ff43`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc698d4c330b08f0e16fda8ef2f08dcf5515555054cd15f1447916f6417e4106`  
		Last Modified: Mon, 22 Jun 2026 21:07:18 GMT  
		Size: 6.1 MB (6062890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:8f5a83eb51e324734511ddb6e539ac5592b33c8e846124ff9e3c40fadcfbbb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f12b8cab76048437250e6c425a2f3e877c4cc4a3cad1570a297d6a6046808cc`

```dockerfile
```

-	Layers:
	-	`sha256:383a1dc595cc7be04c0215692e726d7491f9d3b5ef5bf6dcb0fd78dc44a7a7ba`  
		Last Modified: Mon, 22 Jun 2026 21:07:17 GMT  
		Size: 1.3 MB (1289295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e3cbaf2d3118cdea5dde1c769d0dc21a5996273ebdd10aa133379f8200b8df`  
		Last Modified: Mon, 22 Jun 2026 21:07:16 GMT  
		Size: 17.6 KB (17572 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.23` - linux; s390x

```console
$ docker pull irssi@sha256:7cd75ba79bf4f34ba81e21b2dec21292ca05c7f0a85b05f67240ac33d7bc7223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21277654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78906991e5560a0f8a9186b95ca902141ec50d3deb79cc9a88c94ca37086294`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:46:33 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV HOME=/home/user
# Mon, 22 Jun 2026 19:46:33 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 22 Jun 2026 19:46:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:46:33 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 22 Jun 2026 19:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Mon, 22 Jun 2026 19:46:51 GMT
WORKDIR /home/user
# Mon, 22 Jun 2026 19:46:51 GMT
USER user
# Mon, 22 Jun 2026 19:46:51 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1a3b639533b39fabdf06fbaa13cdd7e421c8fd97094d306c225ebd72c5dfa`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 11.4 MB (11366931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d1df320466adeacca73c2859b76a6a11fb284e7554134179f7ae320cef5242`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a6bf8cb2affcc570d30e427ec2de43d4fb2ee3d73f5b53ba0ee5223aa9041a`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 6.2 MB (6202491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.23` - unknown; unknown

```console
$ docker pull irssi@sha256:b4f20c9d1f6fada462a04d45b3ac9c1d3dca1ec5bf5a7b042b6bf10081dd8479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1306741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799fcdc0bd8c80bc76c68d24e51158cbe0f050aca2015fd3b12abaaec557f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:6190de7dcf0e7771b7bfb8b673b4a53f4d3f23eddd402d10f69b485603bf4810`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 1.3 MB (1289241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea269e2b2b1765c13e969996451fe624a1526ff4e72c19ab4301e5631c796ce`  
		Last Modified: Mon, 22 Jun 2026 19:47:03 GMT  
		Size: 17.5 KB (17500 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:09d4c4a5bc3ad6af824798d462f094111985764b74fbbe0b4cf641c9384b0aa3
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
$ docker pull irssi@sha256:0ac322f6e886f3722e57264aab3061401896ab407a68d9362bcbc4dc2441f4e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5f7e9229ffe991cda8df8bba94d692ab47fd403d7222df572af1365020a493`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:24 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:24 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:00 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:00 GMT
USER user
# Thu, 11 Jun 2026 00:22:00 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927c1e93bd81c2a0f25e45b0c6bedf5dd12c7dd87721b8c06b18db834e71e3c`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 19.2 MB (19229602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700829c35bb7c0aa8a4bc3707ca402702810ae368cc5bfa3eaae004c053d1742`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0233eb1f67b8dbfc0bd526fbdcb770ac9ccf9d9f9c4c95483be9dbc985603d`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 4.9 MB (4867692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1d492a918ed00ba9435f08f8d6ec182e6ee531d1d74d0981aaf77fd36c62337c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f2a1ede778ffd2fdd49305a0c034c38efef4e3bdcb27c0b65f50bf265bc72d`

```dockerfile
```

-	Layers:
	-	`sha256:1c40705e3c602d9eeebb87f4c7e1b845aad9d002ae40f0d0c53652dfd302b0a9`  
		Last Modified: Thu, 11 Jun 2026 00:22:10 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec75c6a10e0c3762e99a773816055de3f0f0d8557a1f38017295ed0bb224e73c`  
		Last Modified: Thu, 11 Jun 2026 00:22:09 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:6a17f731a705ddaa2e12c136c027b24f8862af35a21fdf4b523dccbd01f821fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92d82bc10744ad81a40efe4feebd5bd74673222c262f80aaa1cfb30e07da920`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:20:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:20:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:53 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:53 GMT
USER user
# Thu, 11 Jun 2026 00:20:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1977b51b4e8bfdfbdd1d8b518a440a88e2b6787a58c7d745d78c360c68d130`  
		Last Modified: Thu, 11 Jun 2026 00:21:05 GMT  
		Size: 18.3 MB (18298211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a64424c3326b78655f75398a68b04da3516ad487a4bdc81b9630cf0e23d1ae`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8998577c39a4e4263eb77a4734ec46d38306cef9675be4ebfe9a10e9d1359189`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 4.7 MB (4710460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:997b733539ab8c75b3149d3437e757e95ac284c4b11cdd5dacea655b9bd7d7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcc8cdda2d79b42277ddd6056cb32602fb4d233d599ebd8e9e25d0daf497aa0`

```dockerfile
```

-	Layers:
	-	`sha256:9ea29922f2c415dfd495ba7293bf935a75869802255e27ed554e47f0166f35fe`  
		Last Modified: Thu, 11 Jun 2026 00:21:04 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36db996ce02178298435ca62d8820c9de2c28036b0a22235b2054999fc49a31f`  
		Last Modified: Thu, 11 Jun 2026 00:21:03 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8c8816d12c4206b0b2436fd7a55e18766c31f84f89b19be63acff32144b10eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ecfca2702c2dc3d53f765f9bd477fb725cca76f45640618f444b8014c0c62c`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:21:33 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:21:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:21:33 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:16 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:16 GMT
USER user
# Thu, 11 Jun 2026 00:22:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730fabc3a8730776af8cf752f81c5d511f67fe721e2c108ec3f038f9ea5223fd`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 17.9 MB (17918234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ba6a811a8ae0f31f96e4af2beaa347c7405d28e0fd2a9045186217aefdb7`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684795e8f657220f65086f0ce3606354233d3041941322226e14bd1541bbdf25`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 4.6 MB (4559733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:16fb7016251a176bd26a51b43b2054afc7911620996166b6a6406a062584edff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef21d4dd996c510ae21873d1a1e21dae1e1ae2cc13895ddfc063856a3e31a39`

```dockerfile
```

-	Layers:
	-	`sha256:6562e35a48e8609e2866abdb9d10b0f33c7d15bb6de297371e5889dc011efa49`  
		Last Modified: Thu, 11 Jun 2026 00:22:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4cae0d3af6c5186fa5ef1d42ad7cda951c8f40932fb31d9aa193756a243e07a`  
		Last Modified: Thu, 11 Jun 2026 00:22:26 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:b1e19e0ca456d7111c31b3213e2d19c23fa51eedaf689bf632d2b9de21df943c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5098cae78bcd7fa823b67d02b46444801dc6ca39cd9967be5bc0e2c12cc7bf53`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:22:13 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:22:13 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:22:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:22:49 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:22:49 GMT
USER user
# Thu, 11 Jun 2026 00:22:49 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e2a0fad06eec5c1d9964b3e4088972e05c7bb385778b27056705f3250af5c2`  
		Last Modified: Thu, 11 Jun 2026 00:23:00 GMT  
		Size: 19.1 MB (19055852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0972fc51c31277b46f1fed55e8f3ee863fbd6976ce686195494ca9847ce6f2f8`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef4834e04473908aa9e2bb1ea70b1b9fcf98b42d791ea98d51599010025c6f`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 4.8 MB (4782060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:c0b19727900c1be326be0d9565cdd7c0924fa5ddee32648b231e0193ff3e0eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32c66bf3c503373696394e880f376cce0225fc24e19a09f2ee92b198861bb37`

```dockerfile
```

-	Layers:
	-	`sha256:e4a9361c5c9d974a9451b40691b78b4ab7eefef896998a331687cc1b3dd3c3d2`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c7f94de99c87eee9425f2f66f7cf87be143e5715a2fd5eb0fcccfbbd698454`  
		Last Modified: Thu, 11 Jun 2026 00:22:59 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:3a9911c5d610a25da42d264d3d6a49d1ba4fdafe40e3509e8300d8de65300500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d2fda13d56a2a737e5ac36550fc21193a049663ba5212a88dc1219d1066ca0`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:15:37 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:15:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:15:37 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:16:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:16:19 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:16:19 GMT
USER user
# Thu, 11 Jun 2026 00:16:19 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cdeb0682a7a3e109a021814894ddc672ec8c95656b477c94df15de427c151b`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.7 MB (18747177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5cd0c65c5c3d63c16cbad3af28a9cd8d0407d982432983dd42fd095738acbc`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d26f97d8f0f06cbc63611764529cdee2dcf3d1128b8ae19cdd6187f464c325`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 4.9 MB (4868934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:82b9ac1a9d6178ca02582eb318d7adc03aeed63ac6d28b07715db5376aa21143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c9b89a37dadcfd995952d58342e106d74ba8e957f1515cfe710e13e11e73a8`

```dockerfile
```

-	Layers:
	-	`sha256:924a0ed2d66806d22e4531bd352a3bc7edf9863b453ec60a730c30cc4b778dfa`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c658f2898ca8217fb7e09fcaffa502139b31967134faa2ed70addb6973a1810d`  
		Last Modified: Thu, 11 Jun 2026 00:16:29 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:fc06083675dda7eba274e623de424956aaa7992cfc4798c0104ba9c37fad1c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e77eb4cb65efd04d5bad74e6b21f47bf182af6dd4c515ae6cf97570bd88353`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 02:31:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 02:31:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:31:02 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 02:32:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 02:32:27 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 02:32:27 GMT
USER user
# Thu, 11 Jun 2026 02:32:27 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714cf4881a5a99831384c2d6b33274bcf4dc0cc98dd520581d7d2841dcd13f7`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 19.5 MB (19543931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d70be1af94c515d2e6c2e4b3ca074e90d56ec0a58c83fcb395a0d0db1c83f3e`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143c4113ce5c0411a361642e9107f8f8567a58de5538a10ff52962616f70c02`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.1 MB (5098690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ff1bda949b87d72840bd175b29142abaac74ceb1fbd2a4d34f7b6ac323b308e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bf2b5e986b75653e3a112432d77e14a44781d05f71c2c82fad6878113852de`

```dockerfile
```

-	Layers:
	-	`sha256:0a0e731e99bb4a8d589f419d43054c29acb33fa8b48b23b7252494cdd43d6cb5`  
		Last Modified: Thu, 11 Jun 2026 02:32:46 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89a0e6ae6deed1730fb468ace825d5fb9dcaccabc336f3cc0c1736abb581a8e1`  
		Last Modified: Thu, 11 Jun 2026 02:32:45 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:ad3a19099e783d0be1722a2921e36c048e935092b9c66e975f61cd31770d569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51709977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d229839a1f2d016cd6ab3b5eecc493fe5f0b7cf07d057d623fe4b211fbf8b5`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 00:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV HOME=/home/user
# Fri, 12 Jun 2026 00:19:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 12 Jun 2026 00:19:35 GMT
ENV LANG=C.UTF-8
# Fri, 12 Jun 2026 00:19:35 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 12 Jun 2026 00:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 12 Jun 2026 00:26:28 GMT
WORKDIR /home/user
# Fri, 12 Jun 2026 00:26:28 GMT
USER user
# Fri, 12 Jun 2026 00:26:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f07098723eba4f0aac323104a9b062d1eec964e3c190e6bb7b471990a04aab`  
		Last Modified: Fri, 12 Jun 2026 00:28:25 GMT  
		Size: 18.6 MB (18562906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa08f89e69bae31101512df1c294af583e006be1fa579bf4b1e043b5fbc7bd2c`  
		Last Modified: Fri, 12 Jun 2026 00:28:21 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61134a9dd08c2b51d0a0b5c5a2f6dd873d15a6e9d7d9d90615273a2d90bac43e`  
		Last Modified: Fri, 12 Jun 2026 00:28:22 GMT  
		Size: 4.9 MB (4861405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:106b4873fff31edd9be6402265e84decefd57e9ce9a15329ef95f67c682ca6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33c013a54e5c9f631e8570bb2c307cf77b14aea13a93a7919b4add6cb072be2`

```dockerfile
```

-	Layers:
	-	`sha256:27019a00a6c03135132a3d28fa5347b107a4800b587fe6227a1a0388429d646d`  
		Last Modified: Fri, 12 Jun 2026 00:28:23 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0aae596812acac1c306b0e85c2acbd9e4f77696d4ae1ef76ccb3d2353092641`  
		Last Modified: Fri, 12 Jun 2026 00:28:20 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:44c5141ba1cf97594d091d5d15e91d97b116502c12a2c1917bed1131ca47a4fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc29355eda1b4b31e3a1cbb41e2f57a77d514d089df25e1e7c25deae4a516a8`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV HOME=/home/user
# Thu, 11 Jun 2026 00:19:51 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Thu, 11 Jun 2026 00:19:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:19:51 GMT
ENV IRSSI_VERSION=1.4.5
# Thu, 11 Jun 2026 00:20:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Thu, 11 Jun 2026 00:20:32 GMT
WORKDIR /home/user
# Thu, 11 Jun 2026 00:20:32 GMT
USER user
# Thu, 11 Jun 2026 00:20:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701a16f6c70a014811cf05e72deb9c037da1689e2573893f2224da5d1c8f7d3e`  
		Last Modified: Thu, 11 Jun 2026 00:20:50 GMT  
		Size: 19.8 MB (19777038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b509b8be811dca4cf036b4b94b40c3f01ce7863aed086e2935d5270f9548373`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a787929ffcf2b8f8d597c4c257a9cc9ab658ad94e5d41ca3b548cb746540327`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 4.9 MB (4906897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6f0192942ff9a70fbb1bb23a8b60dfbbc181264ec9726e9fceee01278380fc86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a73e433d32776fbb615ac9aefb539c7f034b7b76e8804c3608f09ccfb1a9199`

```dockerfile
```

-	Layers:
	-	`sha256:8994362453f746ea854fcb3a1189e3c1cd4d11d842a4ffe8b02b9f3da12dcc61`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b71ad535f357810a80bf26b7382ffcde487a632b61a9c12433cf6b9f1729fb`  
		Last Modified: Thu, 11 Jun 2026 00:20:49 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
