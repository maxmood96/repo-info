## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:d2fbc09ff32f572150e83656f6a5c1e438041a35e70645cfdef5dc7fc835b208
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
$ docker pull irssi@sha256:2ef8a256cfc2be2cf2d92c4d60860b38c15a5aca93230ba73367f6ed42f83f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53886197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eef4651ec187e2c741986f8450c57c52d38773589da9ab9a20ef789a880ac88`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:15:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:15:47 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:15:47 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:15:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:15:47 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:16:22 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:16:22 GMT
USER user
# Wed, 24 Jun 2026 01:16:22 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f098f3c1de6f0f0c785b852a6cb00937833af3cd231ebf3487364afc958bc5`  
		Last Modified: Wed, 24 Jun 2026 01:16:33 GMT  
		Size: 19.2 MB (19229743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6108ab960ff8befdc3d1f4f8914ab37818071fd0fe359c27359f3f116072e9e0`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5831d9595e632dad393e40b1a04300c155679731f7562bff82c26bde16ef9b3d`  
		Last Modified: Wed, 24 Jun 2026 01:16:33 GMT  
		Size: 4.9 MB (4867676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:3d464a75e2b9cd47bc7ae3265ed78f0054495139bc6e1fcb8625100b8b6d7b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90746b56bb3b1b6adfd3d4758062416b11a777c4986763b80a63c8a0b4a022b`

```dockerfile
```

-	Layers:
	-	`sha256:d2f8f73b02f5e65be6fe56cc43a5b5209db33972c2f47b4721ca8f8c0c74413d`  
		Last Modified: Wed, 24 Jun 2026 01:16:33 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f8f6ef78be148472f3be6090e79ba49a9f068cee6cb70aeb89b29061fcae22`  
		Last Modified: Wed, 24 Jun 2026 01:16:32 GMT  
		Size: 18.7 KB (18651 bytes)  
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
$ docker pull irssi@sha256:c79731a3d86e3b4ea9b139a38cbc9b7dd7785a3439e19ec99968fe674e0c80b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54920600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f471eb47009cbea5d5517ab651a05fb8d2909f4d37f01817c4a4d8137f6ae1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:16:32 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:16:32 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:16:32 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:16:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:17:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:17:11 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:17:11 GMT
USER user
# Wed, 24 Jun 2026 01:17:11 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0a7b85bdc61e23fe4edf5328983889a4532c723a3c16bb1fb82811d7a665cf`  
		Last Modified: Wed, 24 Jun 2026 01:17:21 GMT  
		Size: 18.7 MB (18747119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a78a7db65f5c7fc7371bc85c4255e57ec66965b1a4cb140aed86c62e78a105`  
		Last Modified: Wed, 24 Jun 2026 01:17:20 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d40e5193a5d57b8bff4c86cd09514888722d43de9efdbf111bb058b5801c3f`  
		Last Modified: Wed, 24 Jun 2026 01:17:20 GMT  
		Size: 4.9 MB (4868906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bff8cb3b55487ea4ddd01494c23d9b4815ee25a8aa86429229dcbe1adc62c35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efee0c5993099bc0e33cf0da5d8ee1e949c050c0c3a3c2aa5de94af9651deb9`

```dockerfile
```

-	Layers:
	-	`sha256:adaf948308b73fc9351880d5e96094161c3f59aff6505402f72cfb268be73122`  
		Last Modified: Wed, 24 Jun 2026 01:17:20 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea52efff25848c2f2ecfb75a082d6c51653b4114bf3dcd00cecfa5705e0eb1b2`  
		Last Modified: Wed, 24 Jun 2026 01:17:20 GMT  
		Size: 18.6 KB (18593 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:8497783ffb752c673b40bac6e26969894f93c9ce17069bf7daec9883d5197bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58252491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c2f1613306f8e796733529cec601d355d48a9ce4faa7fb56902a35abf6c5ba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:25:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:25:16 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:25:16 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:25:16 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:25:16 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:27:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:27:13 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:27:13 GMT
USER user
# Wed, 24 Jun 2026 01:27:13 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1000292e2d94490eb5ee5b15dced71b72de57eadcc0bc162536bacd41dade55`  
		Last Modified: Wed, 24 Jun 2026 01:27:34 GMT  
		Size: 19.5 MB (19543975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679bc2aa3b1163339819bfc7defba6c9a247cc115fcfa314ae44155a3b6c6706`  
		Last Modified: Wed, 24 Jun 2026 01:27:33 GMT  
		Size: 3.3 KB (3336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f03b14f3056fdd8d161cf7ca10ac58974d0e6639e5806904e2a62016885335`  
		Last Modified: Wed, 24 Jun 2026 01:27:33 GMT  
		Size: 5.1 MB (5098760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:dde4452acc23542a3c46c8f4c300ec075686efa667b5500ae990b2f8d687877a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e9782f2c6a668a51e112046a6cd09cc4bfba6949387fc673f3b997df0d99d6`

```dockerfile
```

-	Layers:
	-	`sha256:c0ecf4e906a56239646c3a7b4a46934d68b7e699bd32ce49e9416592dc6270e1`  
		Last Modified: Wed, 24 Jun 2026 01:27:33 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8b0b20edb7219de658a8ba9d5fb396c88c91b1642bc33032eb1b27bdca339d`  
		Last Modified: Wed, 24 Jun 2026 01:27:33 GMT  
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
$ docker pull irssi@sha256:32bf5f073f62d4043be0d906aef4675beb8081c29134244be56b434d347be677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54538238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766dace219bf7735cbd74a21a948702cc85a3087448b8757d7e4da663822bbf9`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:18:07 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:18:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:18:07 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:18:07 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:18:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:18:47 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:18:47 GMT
USER user
# Wed, 24 Jun 2026 01:18:47 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48bebcdb184f28922d9a474ab4af51b5adc15a1d39bc3538b11e2d2d332ca8a`  
		Last Modified: Wed, 24 Jun 2026 01:19:04 GMT  
		Size: 19.8 MB (19776551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667be9254fd49c8ed6ce64d9061dddbdcbec5e530b056331e49f3548d2fc5f00`  
		Last Modified: Wed, 24 Jun 2026 01:19:03 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44896948d5e8e045a19e6868723be737fa4f373c81881b0a48754fe48f78832`  
		Last Modified: Wed, 24 Jun 2026 01:19:04 GMT  
		Size: 4.9 MB (4906945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:9b1878c6f6bed51ce74efda68de885513f95a26ba5e5a1d3b895ae8696491a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076a7fe1529b6d6738e0939baaffa5803028b524584cf72df98a7428aa18b45e`

```dockerfile
```

-	Layers:
	-	`sha256:9781b17a837f6d930dd660afe6866bcec44d8c1b91f2c0867b9560adec98952c`  
		Last Modified: Wed, 24 Jun 2026 01:19:04 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d6078493e9d9a50e97f2595be062a24ef08334063e2178a74983af7c3711f8`  
		Last Modified: Wed, 24 Jun 2026 01:19:03 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
