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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
$ docker pull irssi@sha256:d2b47ae2c5affee2b9082f2b388ef35e5345ad0a8af1b7f8a544af2b19727b78
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
$ docker pull irssi@sha256:18ecc964fa9fff99cff21709697dac6fea3f77b80e9c820a6554afc0d7edd2c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51704875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff144164880483aed6d8aa69ea6295ab148bbf00e11cf5be20d91014a93dc94`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV HOME=/home/user
# Wed, 20 May 2026 03:34:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 20 May 2026 03:34:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 03:34:53 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 20 May 2026 03:41:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 20 May 2026 03:41:45 GMT
WORKDIR /home/user
# Wed, 20 May 2026 03:41:45 GMT
USER user
# Wed, 20 May 2026 03:41:45 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bde908e00815e1135ab76fe3289be582b31155d86272f1e84263a4553e5e88`  
		Last Modified: Wed, 20 May 2026 03:43:41 GMT  
		Size: 18.6 MB (18562561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b8876f82ad8f3661a0c4a07f46d0b493debfafc6f30a9daea9a349f30700b7`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5280bc2d5c83e084ba8f38f9b95cf64fe0939273e1ef63537df3d43859d52ae`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 4.9 MB (4861355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:f13dda61f4493bdf8a0455ef81e6907e875f255fd9838d09349dd873c0e29aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae5d332620cb8a34b9d579deef994aca4fbaffd45bc70a5c182f23978540f6`

```dockerfile
```

-	Layers:
	-	`sha256:64cd95c04e3eaedfb184de86289ae7cab0b22d728e3b61c2f6034e3ffa867d72`  
		Last Modified: Wed, 20 May 2026 03:43:39 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b03941debf46b9d5510a01813e3289583da8c25b793275879422659ae30819d`  
		Last Modified: Wed, 20 May 2026 03:43:37 GMT  
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
