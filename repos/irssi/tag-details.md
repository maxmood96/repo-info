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
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
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
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
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
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
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
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
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
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:trixie`

```console
$ docker pull irssi@sha256:a38e47fcaf4e1dbe80ce22b1f3a07aa11330415c2de04bf8e86918258f332cf6
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
$ docker pull irssi@sha256:4d7f59cc5a76087042c6a8ba5d778e00f5b8021abb89d0ad60538c895478f70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53880407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d423da848263bd74b4a6b5fd61fad3ac1bbe39e648a070c3c9efa4304b3b1f`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:01 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:04:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:04:37 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:04:37 GMT
USER user
# Tue, 19 May 2026 23:04:37 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e0baf300942de3b7ac05b2bce053f9cabfb40f4896491783e75de7618de812`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 19.2 MB (19229490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5ae0874e8dbe63e4708003aa6ab24453106096991d86f2405bd10e9dac715b`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed74f74ce40965bed4dc4204db1511202da3f797effa5198a18c1d42ca62b71`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 4.9 MB (4867626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:be4695989d4ff7aba20f8c243f5c3e6172e063a8d91d76913d10a1ee8cd201d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7c31abab05b5a80bc555f1ceefb2add4fc46c119a5d826155c28f077b8b402`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5ae26925d89f32e8ddde4d9408b2bfb5cdcd4a117a53303e3c9d108dec070`  
		Last Modified: Tue, 19 May 2026 23:04:48 GMT  
		Size: 5.6 MB (5588553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f6c2ffd934578c7083fdc1fb0db99623d61c7be5b14e4f1b398b71be7c06e23`  
		Last Modified: Tue, 19 May 2026 23:04:47 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:35733d61d03b1601377945f38a5e99644eba6d67c81d0042284d0ebec89546cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50966115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d11b4bff73e8d4a6f32fc44ccb15fdddeae896112ddc39b0bdcb05b05950e7dc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:59:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:59:02 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:59:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:53 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:53 GMT
USER user
# Tue, 19 May 2026 22:59:53 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd079ce471df07d2855cb3fa2aec6d87ce43effe69a4cec25f1c4e3235b085f`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 18.3 MB (18298209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a97886491e3194da659206ff1d0d92cbbf1faff855d6ecd4a99e3ad91a48794`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae540dfe1f25c4618f3de1f945c41af65a3daa900bafe231a7ed927ae7a58d`  
		Last Modified: Tue, 19 May 2026 23:00:08 GMT  
		Size: 4.7 MB (4710672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6bab37a9e9dbc187d539dcd6a5c9f509ff91d2f7c8b833a9e7f4ddd47176bba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396701c9dc49cee9419bdd0566f3e79e75efe381fb30a2c509253ee116df8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:a51d48f633fba108e52f3dadf3c5fdf9cb37801fd4ab90d5ca6b413846f376da`  
		Last Modified: Tue, 19 May 2026 23:00:09 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53558b29474f0cf25c9a1a20ee1224c0f89e07345182c61ad45d87b074c98a`  
		Last Modified: Tue, 19 May 2026 23:00:07 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:e265635024e24009346bb5340007a3c7b33f1e613eace54a639a501759d22658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b00110abf379027242e2b3189c70df0f5b124f61b546f3aad943a19869fa74`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:26 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:26 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:26 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:06 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:06 GMT
USER user
# Tue, 19 May 2026 23:01:06 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46994af277f9d2c300a4c91ed293ccbb9a28db1484e4fbf42a294bc4c8d195f5`  
		Last Modified: Tue, 19 May 2026 23:01:28 GMT  
		Size: 17.9 MB (17918124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adf940325acca801d4ccdf660e62fc165dd5464d1b1c60aaabf2cd7241f419b`  
		Last Modified: Tue, 19 May 2026 23:01:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f8aa41c2e52d3ff170c7cbedf40dff622078e7971710d3ee6db136f22f2346`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 4.6 MB (4559946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:21f395b935e388e746b8f5c3831800edfac67af2b367ce0db1e53a351e902549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e037b7505a90a6d28d30bdaffcc4c68fcf55c05476a2453141f0b3988e11faad`

```dockerfile
```

-	Layers:
	-	`sha256:0a14fd54557287b6c2dd36fa8761367f1a1d338fac47b8763ddd0addd9e205e4`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14398c44c4c3a91c3f1db3fe1837d0071c9c10cf04fe301e96e87d6bdc2ff87b`  
		Last Modified: Tue, 19 May 2026 23:01:16 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ac7004b3b999c1196bcf9288255a9d885e921779bc8b472465d8af48408f07c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53983350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63aab43ed92771bb9c6aa86e440cdfcd8242544bf657271eef04920fbcfcfae1`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:02:43 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:02:43 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:03:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:03:20 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:03:20 GMT
USER user
# Tue, 19 May 2026 23:03:20 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4bcbcd172d144cc4f706a2958fb8e3b899df7d230278274db6417761a36178`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 19.1 MB (19055894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf05343ddeeca490d8069a257682059cd5c1e485ad2f2d657fb4610d079b9a7`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d15a6bb7f347e77310a296ddc6ed87eb1ef9f7a05d747bbd0f9e0218e63bf8e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 4.8 MB (4782172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ea5267a1448362c285cc1a79d947c698a00bf6b385c54ee4e19d5dea04912d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006623e4f34f338e3905c47b1738899a6510b86457d215b86c7732bc43ed64af`

```dockerfile
```

-	Layers:
	-	`sha256:f5d3c1691e8282250673bd246509af3910f43df0847236c73e89322f99f194a5`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dadafdc98b14414a476b203e7c92d3a97037e95f032c00abce41db0e0a2925e`  
		Last Modified: Tue, 19 May 2026 23:03:31 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:87a4e748d11da0ebad8fc5c6b15291d78223b387bd5fb29b5d9706c7dd20e726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54914701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7546ec5d1985c1b0c2dcf1222a06e135891646fb659f01d189fbf5929addf2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 22:58:21 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 22:58:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 22:58:21 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 22:59:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 22:59:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 22:59:03 GMT
USER user
# Tue, 19 May 2026 22:59:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99afdc33d5a1f1c5ce2212735634b849b2ec025b82de82c7b3078c4b9de42c9d`  
		Last Modified: Tue, 19 May 2026 22:59:13 GMT  
		Size: 18.7 MB (18747097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c022e38eb84d210a4f44f43f1d18e17eb0b1cff0ffcd8e029957bd00126ba6e9`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d815665b6004daf0250faaa07ca04f5de5423bb4d82b588f9980e0d4fec9d13b`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 4.9 MB (4868907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:51295af1bfd40f19f9835c5315833d3476d2ee67d83a3be237abf315926ca44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384132b1d9212e97291470d842ffc35e2010089b37844fa180dc5626084199ce`

```dockerfile
```

-	Layers:
	-	`sha256:e4ea190ecc9b152c8c1093f3e182e3a63fd3a6ab42a863f7e58799008fb15d41`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 5.6 MB (5584676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fe70c2eed673bc7774b04af2ecd1ff10f3d5c6b2c45a5fe4f022507cd860c`  
		Last Modified: Tue, 19 May 2026 22:59:12 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:ac9b03bea0c93987f4054ac3bd816ef4e929d3ee0b80398d90ecbdef2b262095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58246357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327989c2121283d1a5e49d79a4ecc600caa8b02708b6237be10c5199754bce90`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:04:45 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:04:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:04:45 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:06:03 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:06:03 GMT
USER user
# Tue, 19 May 2026 23:06:03 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7986aba57277ddb0e37928b6f94ea58c6f74974442eaf1cf49e3584bc289deaf`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 19.5 MB (19543943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18b293fd41a612fa645e3b0a0ec7524baa07d0b15ede0d874ae1e75a9d138e5`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d694e4a32978715d1696f2dd7fff6e1f2740b9dfd09ca09d36dec3b85a1ac08`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.1 MB (5098600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:12ba2fbbb4aadf035bf0a4fc43742177ad2e924debd6fbd2533f8488e13541d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0eedcf3d9233b221dbd96e39e0fc5eb9c6c37fe0eaf97c84313f84e0c241f73`

```dockerfile
```

-	Layers:
	-	`sha256:4b5006b8c5c12b9bb3d80434f003298007e0f7c0a02b957a884c9ef5ffaadb60`  
		Last Modified: Tue, 19 May 2026 23:06:24 GMT  
		Size: 5.6 MB (5595584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c6e70e9bbe6f39244e0d4ee7087502b59bdafd2b2da4959e6d954f236687d1`  
		Last Modified: Tue, 19 May 2026 23:06:23 GMT  
		Size: 18.7 KB (18722 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:44d50e8815b020998ca50b41db383d4ae5ac716ad7cd222460cec78af72f28e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51699237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c63d179fa9cd5f012db84444f9e67109e6cab3b925d577c978428b4a8b50b23`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 16:00:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV HOME=/home/user
# Sat, 09 May 2026 16:00:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Sat, 09 May 2026 16:00:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 16:00:34 GMT
ENV IRSSI_VERSION=1.4.5
# Sat, 09 May 2026 16:07:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Sat, 09 May 2026 16:07:18 GMT
WORKDIR /home/user
# Sat, 09 May 2026 16:07:18 GMT
USER user
# Sat, 09 May 2026 16:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679b8e9bc5b7245be29308423f5a95e4d8f0470a07a70ddd731ff095a2d8b87b`  
		Last Modified: Sat, 09 May 2026 16:09:13 GMT  
		Size: 18.6 MB (18554906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e59410009320eac84c029a82002fe527d74ce2964f757a284c3524a0608391a`  
		Last Modified: Sat, 09 May 2026 16:09:10 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f668d15e1969f6f60e13f8cf76a03c2209cb977071a91c26ad3ceedb8eb41b53`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 4.9 MB (4860734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:11f71879c3d2cbaab001cbdac857547701ee2e906e72cb2560e919aa566f7546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4a6abbf2c96c3757fd7c2c416caff6b3da88b6e9d4aa4d236f4efd7f7e58b9`

```dockerfile
```

-	Layers:
	-	`sha256:816c3242c901d897460023a8d3e51b6efbee5053c3ee08ce84083ff89c72d3b6`  
		Last Modified: Sat, 09 May 2026 16:09:11 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1dca4563385004f9084c4b8cc6fa66be6c56aa8174b1058bcf310d2139c8501`  
		Last Modified: Sat, 09 May 2026 16:09:09 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:1b215249fe04707dea8e67553d813643f7b8067ec9c85a1ee563542777cacc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54533083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e09a85982563a1e2da92428dc68fd878d979c9b3a121aff3e052247868b725`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV HOME=/home/user
# Tue, 19 May 2026 23:00:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 19 May 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:00:20 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 19 May 2026 23:01:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 19 May 2026 23:01:01 GMT
WORKDIR /home/user
# Tue, 19 May 2026 23:01:01 GMT
USER user
# Tue, 19 May 2026 23:01:01 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16df1419c134edc35be0e999326d26592ed0703517dd4f7d405771fb55f69af`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 19.8 MB (19776909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3aade193be4d99c3f7553ce7105a2a51a60c3460d2f7f973e33aacd310b852`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6f6fd5537e9257b36dba9471d8a418722de947e164c2098c490b239a9b4888`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 4.9 MB (4906886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a6c2eb5cf3d2a594668c1dd77d1418e2453230dc2953fa54dd57f98bef3739a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ae267a3191b6a8cb92a9e76c1196197cef055dcde8092f1b09c52296c926b8`

```dockerfile
```

-	Layers:
	-	`sha256:392ee5b9ff2720010f9f7c35429c4ee39fcc1157279b71d0ef698c58566a3679`  
		Last Modified: Tue, 19 May 2026 23:01:18 GMT  
		Size: 5.6 MB (5589458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1f0f8118a607f822959b323f433bd523b50c59d74dd7cdf20c32d1cd725ca9`  
		Last Modified: Tue, 19 May 2026 23:01:22 GMT  
		Size: 18.7 KB (18651 bytes)  
		MIME: application/vnd.in-toto+json
