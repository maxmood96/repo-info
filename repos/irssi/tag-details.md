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
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.21`

```console
$ docker pull irssi@sha256:e044e20204f631dd2186ae408a71efe6c7f4ef3a4a2999b3206ccd588e032dad
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
$ docker pull irssi@sha256:4748a9523efd7ad5e571bd0054be2ad5cc3c86ea9344db86c5507a6ae24aae74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (19979940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2ff3b0f7ff9ea28fe207bf24c6e6f3046e0ca0a279c89f31e688e95651eb7d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a38bfc2d597756d4a321e44c9e0a91a67cd08183dfb8af420223e7fa0c8a71`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 10.4 MB (10392812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237d6c6e1c90d16297977aae98f4ae001ffb2336e6594d5baf584f8ce9e6e02d`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f05e25b5e5bcccf5dfab654c841d98bc8ca752f588c674de29908c449a8f68`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 5.9 MB (5943896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:6042a7721a96cd762dba40daa97c2ed27d04ebb3f53427c3791496e47d2bb4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9787f0f2a63b17a7dd1ba0f31903459e8b0936cb8b2b16e88f72f56a2b8b7f`

```dockerfile
```

-	Layers:
	-	`sha256:92067c92382deb8c81591fa8284e5b798a7c6acfe94791770c31c98141835c4f`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 1.3 MB (1268418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbe10db2d36ef35a68cecfd063540f02425d725f00a629707b55e725a0e2753`  
		Last Modified: Fri, 14 Feb 2025 19:15:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v6

```console
$ docker pull irssi@sha256:a89820930ded35d6afc070fb60f1a0db948d89660c5275402433505f7625a921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18764181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c1996338bc71e5f07b6e13cf88e04f36bd69fdee4ac76ba62ac196fde65472`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
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
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0888ae2cdca89cc78164bcf512e2f3d00fc020b432c1a419243bc4899cde30`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 9.6 MB (9620265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5001798eff1a2cf69148195afb4fdcdc358d26ae176c9bc8b3615e3ff5c37c76`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b75eea963d31e91eed8ba6302a1fd58ebe0701230cfeb5828f4702223d8d49`  
		Last Modified: Fri, 14 Feb 2025 19:56:06 GMT  
		Size: 5.8 MB (5778198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:edf54cc1f5ff132c46e6935bea28e5aa41ca0d6c923e04aaa6a92a750b0c1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fe1f870f8d5e56c2b4bbd22280c2216b2056385ad09064299fdcfdc159d7de`

```dockerfile
```

-	Layers:
	-	`sha256:c10c01e4fe162eb306d57b594671db19266b316fdc06db10a4b09550961eff10`  
		Last Modified: Fri, 14 Feb 2025 19:56:05 GMT  
		Size: 17.5 KB (17456 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm variant v7

```console
$ docker pull irssi@sha256:34e9d2b1c7b0cfedb76fc419c37040944a1e803f3f561494dd9362b3e68e6c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18086861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46239683398c720c978cbaa9ea46fb10380cfe9aa4e1566b41f86d9d61e9c43`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
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
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3a8d861f01234dbaab30b0267490984cb949cf6764343672723912a313ec17`  
		Last Modified: Fri, 14 Feb 2025 19:38:37 GMT  
		Size: 9.4 MB (9447584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7211d1720163c8c1f986e3535e818631ceb61ec2e0e46cda7b615316028bb2`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800eb157d88e1c35f3fe74918f3c052081001b6adcaadb84f9c4e2161a8ab13f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 5.5 MB (5540169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:a2785e2172c12a98e26d106a36d1c93032c28a99607a42cbd812349e456d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee20e5e77f2e40c88c1a6c5a98045a0248a31e435b176f04d64fd6cf592470`

```dockerfile
```

-	Layers:
	-	`sha256:cbc3fd43aaed73da39b27ca1af797f258d8619afbabe0179667996a902f9ed7e`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 1.3 MB (1271299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b7c2f8a8aadc86c40243fc3432a86cf357f600ddc0e8475998bd7284f17c3f`  
		Last Modified: Fri, 14 Feb 2025 19:38:36 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:15a870058a595f90c9e2e453f5801cee62226422f532dddf8c8bd5d0c62a3da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20169976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72ca81bea8d7b79e29ab21558346c433335bfc3565f94eedb51a3ca23e84b8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b981c9ebe5c1b087c7f5a60fe604531792a67625f9323ee20e5d56614da2fc79`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 10.4 MB (10354498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea173e5e0195e4bf5c9f49f6841549416fe0ee9a21f3c6ab0c77bee8499a92`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01243d8b0f3a7bf818e2b92bfa21b2a7dd532c451e89f058fccc98e884ca3922`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 5.8 MB (5821465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:242ed530667470d6e22468ad4c50c3e6f204fef35ba46196348b73f5b4d188e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1286247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e5633582ada2e40cd16b7e5e08c3543f8960cb4b226e67b01f22fe1790b66`

```dockerfile
```

-	Layers:
	-	`sha256:4f3b72ba066d68946120e2a8f68b2459f152c2c88d7c9f95a1e640401da96754`  
		Last Modified: Fri, 14 Feb 2025 19:47:43 GMT  
		Size: 1.3 MB (1268522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e77ffaa9a22727ca63171b1c98483929fb4529db31f813462ad362fa16d3ba1a`  
		Last Modified: Fri, 14 Feb 2025 19:47:42 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; 386

```console
$ docker pull irssi@sha256:14007f5e9c1513b7e6d90218c55099cd88492b09d42fd37b089a2213d745aa21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19434679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e4fba7d214edd7f12eae85073bab5450764f1c7ace44ba97a608f500598606`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
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
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b002153264942031cfcc418ced6b2fb35234739687aa4ed9a2667257caff4582`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 9.9 MB (9937487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71a4224609faf9f505baca9d1bdb385cc8fdede5f399f1a5330738a61e2aa1`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412ed735fcbf1ffe2653825825a8234b7042c836847438d3a7e7e14bca52cf0c`  
		Last Modified: Fri, 14 Feb 2025 19:16:56 GMT  
		Size: 6.0 MB (6032584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:d34f8cf8774bd94dd5bc22a94036e888e8c9f07531516579d03bd2928c4a454d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1285856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a6eb0e0265879a066332830c4d9f4c9c5430d83e1cb13ad68b5c128dd9fd03`

```dockerfile
```

-	Layers:
	-	`sha256:5dd081d431dc2f53ae5027a27f4483a97e9add6ebd0a4805c53057710375f154`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 1.3 MB (1268373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08119f63c03ac59bc75e0ead8bef0c3445c8936a799c527044f75ccf28217d51`  
		Last Modified: Fri, 14 Feb 2025 19:16:55 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; ppc64le

```console
$ docker pull irssi@sha256:e7487344d9e405c75993fc9b59892405bda5862471947185d0ee2097720e0c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20373137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec46a052f4f05e82e18f1de49b2a94e7d44d4493e987ecbb4e0b027b952a8e8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422da411020183ca0643d16f0b4e7a2346688f840b701999a37273255bab860f`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 10.6 MB (10591895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914453fe94aabf8cf3c1b10b4cd69ee9a01fb507d12dcfb8db322f953425ebf2`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61131317438f9c0ba4677be9672c352d4d2c99afc39ad9abb4b6faa0624197c4`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 6.2 MB (6205911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:e0ad94f6acc311f89da21b6b5bc04a450a55a196ad2554445b80dbe5b7ccf1b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c816e8a24f78f8c2b4c6334498545b988fdcdb9c9f70022c5ed990c7636956`

```dockerfile
```

-	Layers:
	-	`sha256:a2ef753a96a6adef214e8967cbc883ee54ffd8c68cf8d52c2bdafb280dc9b00d`  
		Last Modified: Fri, 14 Feb 2025 19:40:01 GMT  
		Size: 1.3 MB (1266525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca059bd04310f8a29255a61b6483b67bcffacc7d2edb38d092620e7d43be5a3`  
		Last Modified: Fri, 14 Feb 2025 19:40:00 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; riscv64

```console
$ docker pull irssi@sha256:3de44e6e54fc6a32c0e0622cbdf8e769c77ec656f55906513a131be87ba891eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19147082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abda5ee9850f3181eef0723376a74fdd25f89e98c972b7164788318b8a5976d0`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
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
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de03107dfdb4c78f9d55064c85af55590796df828f0d2fe3474e39298a1c5cf`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 9.8 MB (9836722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88445d5410af344524c9910d6813c679493766891bdb20237ba64c393036461a`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02da64754402ea8844b6ebe04f91418bd71141b2fafc7fbe1dcaaf2d2032e167`  
		Last Modified: Fri, 14 Feb 2025 22:19:23 GMT  
		Size: 6.0 MB (5957937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:c460f9a71f0daa631676f6bb6d4d2213d1c7136100768f054c5c4d73885011a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b53132a8ba26e3852de2210d8ef250673111a64a50306460b5fd35659b9c2cd`

```dockerfile
```

-	Layers:
	-	`sha256:aa73ecae4c64abf7e40559c623f7a7d80d1c90ad122db4ead358fe39d4cc1b84`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 1.3 MB (1266521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa331d0a4d6e34a2a5cc3fd37cec1b0d45be4f85f0de4578e860c553291c8fd`  
		Last Modified: Fri, 14 Feb 2025 22:19:22 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.21` - linux; s390x

```console
$ docker pull irssi@sha256:81139897be3935589020dcbd0bcc3dc77e8f50620833d522f1ea43b02ab0b07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20523710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32f19aaf1872e2034e69a0efd433cba4d7be79a32161f99e14b8436a4ffdc61`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 13 Dec 2024 00:52:22 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
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
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45801b75c6566160c7c80cfd21596dafa454dfd3e6ba93bb49f93d069829d1d9`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 11.0 MB (10956088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697833bc09fecefbe33ffcbef8eb5d10931c6bd374b870530560096436f73de`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d344d01f127fee73ae0c883d59e72ee9e20dd1acfe8c019d4c9d38e7eff1c84c`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 6.1 MB (6099070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.21` - unknown; unknown

```console
$ docker pull irssi@sha256:470afbccb2a787f44886518cc4beb93d1fd4be777afbfab7824dac3d4309922f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1284010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd2f52267b0398a31bde20ecded78fec4ba4a618e29bb8ba94584b4276732ba`

```dockerfile
```

-	Layers:
	-	`sha256:334a01fb019adbe0f27f4ab398fa9d86708aeaf9a85ad2282aa79fcb2dbb6d8e`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 1.3 MB (1266467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2663601b5f94b63ff588d61efc8ca25e02f12569d3947a6030c4a9c868a3946`  
		Last Modified: Fri, 14 Feb 2025 19:40:38 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:4beec173f37405d726e1ab719836623baf6776bd3d95acc5b3c0cf38e4280da8
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
$ docker pull irssi@sha256:64d45cd9c40a58a40fbfa4148a22eae1d4eade4855255db3aaf527cd4467477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51052342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51a8e8739b7959220b9c13e1dbd88511bdfd0dc3c97aa8fbe3d78c870737a1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bab4be54f2018d8d9a3f91e06cebd78ac01804f452ac96ef3c40bbccf7b228b`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.2 MB (18228823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3308e754531c62d5ddd8e4d742f8140e2d6a27d8d73335da1b84e7cf56f1c4`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1367d861d0b516b9ed6b0fe7c30293583818b60c522f7eb85bba74596ce840d8`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 4.6 MB (4592896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5565095e208891ebe0837792e52325bc0051a2075c61d443e0798bcb76fa9fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c58ad00bce1f16fb105bec3a88c80bb111feccb9398b1ceff55ffcb2518a2b`

```dockerfile
```

-	Layers:
	-	`sha256:7d160b77db317885009ea2e23f5e58f1603a24b65f0c1d6e6017da7ca84ac83f`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 5.4 MB (5379821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d47b8d94f388953b211d0204a2e32fbe931381a306e928d324cd8c5475d6c`  
		Last Modified: Tue, 08 Apr 2025 01:12:48 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:57ea8d0832fe020d131ff396132eadcf5465eccb0be6b0709367e32afc4d9468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47215197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96ef6b17548f1a3ff5f3f4f42647677403ce120bb44bc03f0d9ff8f53b40a6bc`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74e0a8063d38e1642f061f82868759146facc68b27efd19f79e95d653d74ecc`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 17.0 MB (17009371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef851b7e80966f73e52fd6d56abde9eead4013b6a0f2830afc417ce749b78502`  
		Last Modified: Tue, 08 Apr 2025 01:29:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d48f1b33af625609b6c025f1b9330e1c84504d125e337fb29c434c4d54b9a7`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 4.4 MB (4444650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4605cbd638898cb5bfe0744e8964c96affa2f5a356d24db21ac7aae0cee3e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1537c5d5ff1e0236d0c0dc2de599e71a199f549d6b86417da01ef0928111e`

```dockerfile
```

-	Layers:
	-	`sha256:bb5117e97bae82ab3208f98887bd3a0fb84d427c80bf303467283939299af48b`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 5.4 MB (5381430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4a8c716ee85f986eed83fbed20095abc91ff3633474f1293b9253ba0d58fe2`  
		Last Modified: Tue, 08 Apr 2025 01:29:57 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:76e3a9d7d7193cb41489d5850dad4b79ebe6bfee075ef27cd114d7ad682dd708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44844688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ecaa2479aabf172741293f39b69670a138a44c50bc4d38a2c958e9f970b734`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09616dc67b9eac9d4c601654c0fe19b314394f850fadbc2a0babd5dd752bcff6`  
		Last Modified: Tue, 08 Apr 2025 01:29:35 GMT  
		Size: 16.6 MB (16604312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9948b91467e0a1e562b1bd18b9e7aa60bfbbc09fcbf87ca2980c9990c7198eb2`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0763cb4f8a70fdab75bda1e0007da6953cde3d48aae20cf56c7408ad9afade28`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 4.3 MB (4299150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c704a6719b8ef337a8ed7f4ad9be768fe717aa19c27c795a4e4603fdc1558466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036009de71d2688bf84ff4dea6e30895c5373b0ef19fa4be438ab196ef881708`

```dockerfile
```

-	Layers:
	-	`sha256:32b1dd7f76eb1e44a835c4976801202a285db20152930a025c4138fc1c488b3f`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 5.4 MB (5381179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b800057b35dbc99e885855f7fd1aaa2115e2c919f5ab539f3363d59388d7956`  
		Last Modified: Tue, 08 Apr 2025 01:29:34 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:7952e45262e5ae39bb2330f13087f057ff6f3311866d52e9d694668e1e89a838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50589510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f93faa0300bae230cc4601ee986fa11a3fda9ca9726cb7ece3bd8afd76d41c5`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8f292aebfa57c4709129b83902ae3916f67cd9439b1930bad72f792244310e`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 18.0 MB (18006692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2645d9cbbc6f9ade16aef52f4de78bd902934ddac89976eb30b0e340bbdde9bf`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d23454c6dde20a23ec8c0dd313c37b266c0dfce50487549c8fd8fef3108197`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 4.5 MB (4513139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ee3e24f02a7df28f0a9fc57ac72412b49c3e6bdade12250f56b539129fee16c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5405195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4db145f255a8375280bd0c570ea3c7272db6c732867db94ea6cff1d496b0ce`

```dockerfile
```

-	Layers:
	-	`sha256:cc40971ed330c0dcf910ff05296b7dc1131abb4f6d56a70e9f85ff684ddd501d`  
		Last Modified: Tue, 08 Apr 2025 02:03:49 GMT  
		Size: 5.4 MB (5386297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67dcb5fbd94cf7737996a697921536582c2d4bbaffd282737c0ee290ac664f2e`  
		Last Modified: Tue, 08 Apr 2025 02:03:48 GMT  
		Size: 18.9 KB (18898 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:ed2a76c9a067af7c98a69f299efcf87948dc83894837d252b5603e039b81b753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad21973c7784b03191e805dfac70f06c3b0bae6b005e586d6994cc48342c724`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550474a83218fb4c09bf9df6553f8de6dae046b134a7e8bf3ee265375ab9028f`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 17.8 MB (17768047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5d7f69914d2a1880cf5b9e5dd9d1e43cf82ad6f42e30a9d29ab8c4d5bbe8f7`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2254f6c8784d0b6094665f8c9d21c068672709d59c2ecf499be15e2decc1d09`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 4.6 MB (4606667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ff194aeb9d582381b6f84ab4c55c9a61447dfedd1732780ec99170031a5ff4f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5394560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e4913500636d78cd4751e0d068a2c1fda88dc66958aea28e05a4be007702a`

```dockerfile
```

-	Layers:
	-	`sha256:51c0818d9f738bf9025768227dfe101961ff1c6c42698fbfba67d00f79334ce6`  
		Last Modified: Tue, 08 Apr 2025 01:12:50 GMT  
		Size: 5.4 MB (5375900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5919faba7ea3809657387be5c45277efe3bc303c86046417e2bf82df251a00`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:afe1288a425066773794522d1fa316c530d7851f71210e253051b72d50c8f829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49976393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1300bfa5956aee63babfa7e0356f1c6fca2be6f0d7e169a1a7e4fb073abe013`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da713410f5ce6141303fc2d9815de7c9393c2595ca427fe229f8a7070e1cbf1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:13 GMT  
		Size: 16.9 MB (16903954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19e9ac41d24e8296ef00b4fd3b65fc32fb0d4b1bbb138f9ee153962b251ec1f`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516fafcb921ff49fd95b3d828fa99642663a039619d7934479a1635ab11a10bb`  
		Last Modified: Tue, 08 Apr 2025 02:12:11 GMT  
		Size: 4.6 MB (4555125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:6c92bc2d7f90f18518bb653ffcea86194a11abe89e22e508d2ea41662425b966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21161350543d3c237bdea3f22343ba8ae5a5f575b0b20245ccf2494d21d4e74`

```dockerfile
```

-	Layers:
	-	`sha256:1f8fa9d78d7bdadeaf1bd3dfd01ea36833ea547b65a7f6350b73d6ef3b995484`  
		Last Modified: Tue, 08 Apr 2025 02:12:10 GMT  
		Size: 18.6 KB (18609 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:7c9fb9f8592baef87a783012b812819eafc19cb7bb508f740199d02cde6340c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55622146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c86fa403130a8948a419e835a93161c4dab2b4ced216eed383ed94ea783a0ce`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a15df7318b692a8c05108c1b6303c2831efa56f751261daa1a5791a702abc5`  
		Last Modified: Tue, 08 Apr 2025 01:39:04 GMT  
		Size: 18.7 MB (18721671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939b2b643f70be67a674bf6f984747271df4c4af7ee7f65e1dadd00be45d62c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f744e6d8ac083bd1cc856b81278a62efed80bb0369e2bc8d91b7e326d90f3b26`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 4.8 MB (4828889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9cea14e0e0597433f4f74b8ed86bfae679a2d4615b99d99fba58e92394bb76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5406303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae5a31a63a1b809d22c393124b539ad8f25f71d0db458ed8c6731309f788583`

```dockerfile
```

-	Layers:
	-	`sha256:5a4db2d3a9f31017ba8eeda92ef7aac82b4ec39fe57554d97e7957efdbe6d7c6`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 5.4 MB (5387515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a92a27848319f02e4078b4c8d6aeaa88257cd9432ed0f23b80f02c38b3bc75e`  
		Last Modified: Tue, 08 Apr 2025 01:39:03 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:3f77d29f453c7ce9ba61ff60f29a139fd9ec021874ab744ff35aaf34a86c5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd5a320634123bc0b7d95884c3a389d6afd76c0b34a1a85f3be53c5a2607e6f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864fe7f944aeff31a15c8554e97d5b07b84bf6478a6595a50f8802e5ea038888`  
		Last Modified: Tue, 08 Apr 2025 01:25:07 GMT  
		Size: 18.2 MB (18187437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eef79296415d7d8768dc3f1a598b6b01923fd1a5437dca28ae65e439bcb0de0`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f02b43f96fadcd7d2c77d4f66ed7908d0bc296f67746687001089db2d65297`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 4.6 MB (4586705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:8a6eac5b188ec9ba540cf79a1f816de3d49c6e2653cfbac27971426c6f376b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854759de40b38b9a5c6332e8174f1d70760afe609aa7a2a7873618a097be7cb2`

```dockerfile
```

-	Layers:
	-	`sha256:5b3a8c658830f12d9f013829d2a2286a019d28194674f7275419c9c06802ae28`  
		Last Modified: Tue, 08 Apr 2025 01:25:08 GMT  
		Size: 5.4 MB (5379015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c11ef19055957ad08b1efd11f40fee76a588287a877e7f6a1da54fb51ed36db`  
		Last Modified: Tue, 08 Apr 2025 01:25:06 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
