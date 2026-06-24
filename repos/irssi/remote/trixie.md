## `irssi:trixie`

```console
$ docker pull irssi@sha256:2750a3c38811d5e0f5f17795eb35c0530fa257b9a15641ca1212e0099256ced5
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

### `irssi:trixie` - unknown; unknown

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

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:9c6f984434b55b6ff47d0dc30b6303b32ecad90e9e8406638f181d9c54e3bdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50971224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dba0c5b5e07b0ac1da2faeb8579c34b05bc6f8159e522f91bd57b07f559555c`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:20 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:17:20 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:17:20 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:17:20 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:18:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:18:25 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:18:25 GMT
USER user
# Wed, 24 Jun 2026 01:18:25 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bb59bbdb8b9cce70c84ec128ca16685064828020a9af947be4d8584b8748bd`  
		Last Modified: Wed, 24 Jun 2026 01:18:35 GMT  
		Size: 18.3 MB (18298173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a1e9b9f97970ec42f590bdda3d7e94c2cf51089b6db35d521b26e13d125e35`  
		Last Modified: Wed, 24 Jun 2026 01:18:35 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762a52d6bf7a721055165152fce06130ac2a8f4f52022dffeb1d0add36333776`  
		Last Modified: Wed, 24 Jun 2026 01:18:35 GMT  
		Size: 4.7 MB (4710466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6ae9497babb6d5ed890b2c95e43aa0685bc76edf4f9c8ce3ba0d7be793026465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c1dd9ee64afb13e93cb0ddadaf8dac5604c119d8287f17e17747f65f964175`

```dockerfile
```

-	Layers:
	-	`sha256:75f1ca48f7944ca5ec816284d9f4021e7c9a173d961c6753748a0dd7ca147348`  
		Last Modified: Wed, 24 Jun 2026 01:18:35 GMT  
		Size: 5.6 MB (5586102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5222ffe3b3ecc3bb6362672b768b98c8212bf10ab470f07093f92a81158d901a`  
		Last Modified: Wed, 24 Jun 2026 01:18:35 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:8a09f260e09b4b8e61f51fee37b909dbdc38c2d0263937b8a320ac83d4fd1df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48692459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3e099ec9fda22ced8725eb804242eb1913d08c68eb208c090f549698a82bb4`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:18:36 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:18:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:18:36 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:18:36 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:19:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:19:16 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:19:16 GMT
USER user
# Wed, 24 Jun 2026 01:19:16 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8beb1abd8be4a5a60f09bda3fdf0b401d43b3377d72dce987d68c72a457ec4b4`  
		Last Modified: Wed, 24 Jun 2026 01:19:27 GMT  
		Size: 17.9 MB (17918168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e580be0074573aae7441865a31a6ced2e9274c54ef2ac9216e4c09ad0b85d20`  
		Last Modified: Wed, 24 Jun 2026 01:19:27 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ccd2320f7239f28e6c946ba53ee54e513b54c8d41bb6d4d0ddce411c36e122`  
		Last Modified: Wed, 24 Jun 2026 01:19:27 GMT  
		Size: 4.6 MB (4559876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:ac622be08227a3f33584b18e45144d81e74b077c07613f1676386ae2bb7b590f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1e84d3b17cccf2c99e5d50ca85e668fa0e8cf458396f3672f1acb7ae40fcd8`

```dockerfile
```

-	Layers:
	-	`sha256:4597b5aeb4ee7985c17d8d010854e0c17c9a99592db4b31774b5ca6077b0bcc2`  
		Last Modified: Wed, 24 Jun 2026 01:19:27 GMT  
		Size: 5.6 MB (5589124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db91dfef5e6ca5acb7d7d5bff398c21f5004653c13ca93ed0d33428edf496555`  
		Last Modified: Wed, 24 Jun 2026 01:19:26 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:561395fe06676721509b6290e57a97726fa7839e17e404119f7fd81019beb12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53989884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999db7a06a940a111ba1c7fdca8a85915b4d72cf7c02b9ae3d8627220bedab4e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:20:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:20:25 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 01:20:25 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 01:20:25 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:20:25 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 01:21:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 01:21:04 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 01:21:04 GMT
USER user
# Wed, 24 Jun 2026 01:21:04 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294a283bb72393ae2fbf5f801a0cff8adde691f54cff36a4e90c81b5310e765d`  
		Last Modified: Wed, 24 Jun 2026 01:21:15 GMT  
		Size: 19.1 MB (19055871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d073fd71c18b9761e900a0e5e71724b8da519841571083dc198208d5a9fc9af1`  
		Last Modified: Wed, 24 Jun 2026 01:21:14 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c4d9e1b8aa365ea311ad8dd47691bf0bf39894f063bb3d595908fd5d4dbc5b`  
		Last Modified: Wed, 24 Jun 2026 01:21:15 GMT  
		Size: 4.8 MB (4782101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:64005db4f517d3053ba6b6df65039385a2371403dab68d462925d4f66739bd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a524b64793b3782644f5c8dc2c47efe6262407f24c090a7fac2559f153866e`

```dockerfile
```

-	Layers:
	-	`sha256:4d4346bd8895d74d904ee79eb726ca18bbea8803cffd532ab5dfdec3e9449559`  
		Last Modified: Wed, 24 Jun 2026 01:21:15 GMT  
		Size: 5.6 MB (5595029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f8f5778e72e3d4f25dac5a69a467cca46cfbbb06b4f4ca0860165de3c5f4f23`  
		Last Modified: Wed, 24 Jun 2026 01:21:14 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

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

### `irssi:trixie` - unknown; unknown

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

### `irssi:trixie` - linux; ppc64le

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

### `irssi:trixie` - unknown; unknown

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

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:56b7a30dfa04eaa948916ce8cf668897b81c3c2055ccfbe70cd33dbde35c8d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a00cf966669bfa5d2372939f36da61b54bca6367242c440ac669129f92c0741`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 20:44:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 20:44:03 GMT
ENV HOME=/home/user
# Wed, 24 Jun 2026 20:44:03 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 24 Jun 2026 20:44:03 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 20:44:03 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 24 Jun 2026 20:50:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Wed, 24 Jun 2026 20:50:50 GMT
WORKDIR /home/user
# Wed, 24 Jun 2026 20:50:50 GMT
USER user
# Wed, 24 Jun 2026 20:50:50 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f4aedbdd8327225623c766d0c77fe9c5b424b6794cb6206fa2fda4f8947d40`  
		Last Modified: Wed, 24 Jun 2026 20:52:45 GMT  
		Size: 18.6 MB (18563062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4233f2f6372d1a9fbca680ac9d693cf890853b0e809e5281907c0c12f61847`  
		Last Modified: Wed, 24 Jun 2026 20:52:41 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3931864be5ccbc4edf8d6460040fbf7cd4f2589e83e1bd3ea297640cf36c9bf4`  
		Last Modified: Wed, 24 Jun 2026 20:52:42 GMT  
		Size: 4.9 MB (4861389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:17b615bdadbf90c95cf7f9bbe93bb5d2a66874c4da980ac469177ff223de7039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c283324ad22a4f4b7f61f88d50f8432b1d864b021f0870429f17af6623a537`

```dockerfile
```

-	Layers:
	-	`sha256:0fcb0b279db79ecc85fbadcb0dfaf937db4d65064afbe9d18e687721bf58962f`  
		Last Modified: Wed, 24 Jun 2026 20:52:43 GMT  
		Size: 5.6 MB (5579856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc84877d49c52cc39ef8b73c05f555a4f34a7ec6080eb5c8dbe6a0e13360b6f8`  
		Last Modified: Wed, 24 Jun 2026 20:52:41 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

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

### `irssi:trixie` - unknown; unknown

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
