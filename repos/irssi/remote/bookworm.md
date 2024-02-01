## `irssi:bookworm`

```console
$ docker pull irssi@sha256:ea2f901f6c07c3b36b7a77dbb9a9b512b4dea1df22ccb4e67af70d67d9024f50
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
$ docker pull irssi@sha256:1fb107732764bbd46c9d264c58acfe07a044060954ce283c8c77afcf44260487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75862194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b883e54cab2e2b9299cef79058e1b92d196a72ffaa2a85a8e917bf52179137e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a954a6604df6b603f878202c3c0331d649d0ab5995102778d6510955709ee93`  
		Last Modified: Fri, 12 Jan 2024 00:22:21 GMT  
		Size: 18.3 MB (18259868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe29c6d994a8bcfbfa0ef3cf02b16e82a7f47d12580ad8ceb99d6a61e48b85a`  
		Last Modified: Fri, 12 Jan 2024 00:22:21 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c458574de27083dda5b3161b4fb7f5e5061e7dabc6b957671b3050991628b4a0`  
		Last Modified: Fri, 12 Jan 2024 00:22:22 GMT  
		Size: 28.5 MB (28473043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ace7268cc17f2ee03093d71e8f6d6b390041e35a976833afc59e5d87625447db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30cf80d8d9c65bc08f2c0af9f074b175611da86e24a26cf37511984e4609a47f`

```dockerfile
```

-	Layers:
	-	`sha256:f898d8a9af975c943834109754fe9dcf59b64fe06633377fb7c1aa2a076409ca`  
		Last Modified: Fri, 12 Jan 2024 00:22:21 GMT  
		Size: 6.6 MB (6616820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb6e7d548d074865c1ae885c84601dc435b9551da44cc1bf097df9cf02b37452`  
		Last Modified: Fri, 12 Jan 2024 00:22:21 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:0a2177211d02c4526ea85d422a3b9261a6972d922fc9fb9a8dc536a560e91388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70039934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7c58b8afd3a9b831e21da7ac132fac9fbf8f4a183fc8363428e0a62232ab29`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2e234aad355a61f304982c134eb72c46730200cc475a400c78836ba8761cd52e in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7b3d38e58d48b1d7eb80e8663c89d5f32b423059b0dbee65b1dc132a6d707cff`  
		Last Modified: Thu, 11 Jan 2024 01:54:05 GMT  
		Size: 26.9 MB (26885480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64893497bd1198a8dce46494b4f3348236d09dd16246ed657bdb62f743b9c85`  
		Last Modified: Fri, 12 Jan 2024 15:32:58 GMT  
		Size: 17.0 MB (17035311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d28e43a06170ae93bb633dc4f78ae7e43465dc05b2310b56b895d0972f9351e`  
		Last Modified: Fri, 12 Jan 2024 15:32:57 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40434e6985db73a9d1e5528156027798833b9aebf7843abdc3a9d14d7f17c35`  
		Last Modified: Fri, 12 Jan 2024 15:32:58 GMT  
		Size: 26.1 MB (26115786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:6f9167aa95f5ac820d8d5552d74ade0cfa34fa0641cc9ab50dc3ca70a1795abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c696b730410ed31ac06370b16aa6684d4a059504394f631030aafa8375d5f7`

```dockerfile
```

-	Layers:
	-	`sha256:12687aad47920f04b3481fb0cc45dc911ff09742af12b9e5dddcdbd6271aba7e`  
		Last Modified: Fri, 12 Jan 2024 15:32:57 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307277cf83b16c47035339d523f9c3359ce052d73e1b9fabb0fd60f894cd0a12`  
		Last Modified: Fri, 12 Jan 2024 15:32:57 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:98c3ebf42241a924df2f56e127e24bd4d93f03d93eb853bf7ddcd5923f5ebb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66361693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe66ccc1728f981d5632551e7b40a6292ac6b996bbc3485c39e0c64d34ec781`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff5858c9698812497c26a23bd86cd48a82ca0b58c76abde17546941759b0e99`  
		Last Modified: Fri, 12 Jan 2024 18:38:12 GMT  
		Size: 16.6 MB (16627308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94662437424443a85ffb6a7b030fe01f69ff11dbf0e51010f7d9fd7827510b7a`  
		Last Modified: Fri, 12 Jan 2024 18:38:11 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a71dcdcb07a3c8e09d420c241638e345db02e640ab96b90fd3ebf8c1efa3d49`  
		Last Modified: Fri, 12 Jan 2024 18:38:12 GMT  
		Size: 25.0 MB (25012897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cc46d2d02a186f876f336fdda8e7f2b34fe7816d44a924b0f61d978c64d0def7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf3d319c4ddd2a52f377f99a171d436e67ccbd600115a09f63cda443f263904`

```dockerfile
```

-	Layers:
	-	`sha256:45c454d80f8dbde034b21fd1305292822dbeb0d9ba496bbae9ed18e6581c4ef1`  
		Last Modified: Fri, 12 Jan 2024 18:38:11 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd15aac017e058ed8d19541d9fcd89c99aeda8a47bbbc51090a49aadfcdb298a`  
		Last Modified: Fri, 12 Jan 2024 18:38:11 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:a0fef9172b502d733de213927d18213717c504fc1666ef3e3360be235ed0928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74614237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd0bb25e2110fa14acf17cc9316baf0d70b312579e92ed6c53ef9578308573d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f2447d7fbe75c490c215c6a789f2e9e662b5e66a770b994f92de55811b98b8`  
		Last Modified: Fri, 12 Jan 2024 08:44:38 GMT  
		Size: 18.0 MB (18021904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d398ca01909484ad1f5210c61749e65a7955a1be412ba90f0c6019e46ff4a9`  
		Last Modified: Fri, 12 Jan 2024 08:44:37 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88fb53cebbd7d076cabba1e85b0fc5dec3a4dfd36d0399d2987bef74d8a7e83`  
		Last Modified: Fri, 12 Jan 2024 08:44:38 GMT  
		Size: 27.4 MB (27431638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a1bfd4ed446e990ed09eec7543b38506a03802745d0cc7536f5d7a160baaef3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08459459bc77edcb199b6e29778c0aa08d73c726ade0ec5488d597631d86b44`

```dockerfile
```

-	Layers:
	-	`sha256:3480a47beb4a7699b43069061aa9a994c3679ef79ac383de328a9475bdbef0f7`  
		Last Modified: Fri, 12 Jan 2024 08:44:37 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b13ba62b00722c3e770e80e398850ea0abeb865e1a19c49207c9c1e081f3635`  
		Last Modified: Fri, 12 Jan 2024 08:44:37 GMT  
		Size: 18.5 KB (18453 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:ebbfa70cff484ab32a8b9193d8106ec30457d032b09ee2d2d57a5ebf0657ec2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74064231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ef4c48f3fdfd460f0f73825cc5ee27856f8cd9c361e2f0425049f15c3d4e7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:61bc6da4a8a8247e6b88cf149051dbb04a6a5e6e1ffc5da16a85d1b4f24be297 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:4f1541106f1f6cee2d65a870d8d3fbbaef35e04dbcb8abaa9623a9f7137a6ae5`  
		Last Modified: Thu, 11 Jan 2024 02:22:46 GMT  
		Size: 29.1 MB (29121397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49efa700980928062263c7db4aebc5d82008dcb95a2e28cbcf521f858e92f895`  
		Last Modified: Fri, 12 Jan 2024 03:49:09 GMT  
		Size: 16.9 MB (16933459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce3d28dd946ec79f804c9a2f9665763da3c1809a8b9f1b8273820cb9c35b25e`  
		Last Modified: Fri, 12 Jan 2024 03:49:07 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c4c1d710862b9d82203d032779a8aa4aab6a283a95d4c5d0a01a458bb8af0d2`  
		Last Modified: Fri, 12 Jan 2024 03:49:10 GMT  
		Size: 28.0 MB (28006019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b52d1287ad5c3c077eeee94ac6723ecc2edc95c178aa9e0161d8ff252b0a564a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69df5743df4fda33783a505b3892ae563129a6de7d778c8ae0154a8ee2fcb7ca`

```dockerfile
```

-	Layers:
	-	`sha256:d1f79202ff8de81003cf7bf5fc5ccc93dda6a2402333d1941c91fb942f0a9613`  
		Last Modified: Fri, 12 Jan 2024 03:49:07 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:52806685d1e39ea606334a799a0e80770205ad00176a41a67e09948aa354ee76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81858418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64b64315a6225d4a9fdd50d2cb1890d8b8fca72ff56f1d81114b3ca848486fc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fcbdad385ae78401c4f5aebfeed9ba8edc6adcc9870a328a756cef32458e50ca in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5d34c3dd8c95d308ec07fd694f24411653403413305af18811f2d53cc052f152`  
		Last Modified: Thu, 11 Jan 2024 02:39:25 GMT  
		Size: 33.1 MB (33120536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9c04aad7bf4647f83e09584839c571f44e9afdb47e5659a3aaff7ed05375e9`  
		Last Modified: Fri, 12 Jan 2024 09:13:09 GMT  
		Size: 18.8 MB (18757755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750b11ba7df90cad7776798d158fdb56f4652e33dbb99ef304b92dad57b935fe`  
		Last Modified: Fri, 12 Jan 2024 09:13:08 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8274e328a74ce34b15af67c79c47173e7b1144e100241f365543ace355e8afef`  
		Last Modified: Fri, 12 Jan 2024 09:13:09 GMT  
		Size: 30.0 MB (29976766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:bad26dfd21f93248a48f6101dc60b0b793562ca9017658c4ccbcd509ac271695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257612f12bf0da116700c9b1c9cafa7f3590e1e022599d6829a108417335cccf`

```dockerfile
```

-	Layers:
	-	`sha256:0cbbe3ea9e99deee4150eb8c07373e17c0e71a28494c5a835195d02eeef64c70`  
		Last Modified: Fri, 12 Jan 2024 09:13:09 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edee83efdc8c283003100a99eff26a553cb79e6fed436e98c52f1cd79572ee5e`  
		Last Modified: Fri, 12 Jan 2024 09:13:08 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:57b79e813254b75be0eadc39dc9a7fe144dc47e670511b8412d5c1f54b0cd28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72724228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d02d84be75fd1c47b3efa603e9b84e0a3214fc6e3fb9be9b59de03c1cfe4da`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:65dbcebb09bfa0253ba47edc09622e132326164df51df5626ae3a06a0e5d179b in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a26174f024d942f0adb6db11b3ae9df606c112928e1b40e24779a0fdab24cb41`  
		Last Modified: Thu, 11 Jan 2024 01:50:51 GMT  
		Size: 27.5 MB (27491850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b840c4e741b22c3159376bd4d043c18d1ec3a463f34dfae0f81a1f120f8644`  
		Last Modified: Fri, 12 Jan 2024 10:19:30 GMT  
		Size: 18.2 MB (18207134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4cfcaa8861f339b9f140ce4590337a5efe8724c8ed77b5c3bc9e22b9040c9e`  
		Last Modified: Fri, 12 Jan 2024 10:19:30 GMT  
		Size: 3.3 KB (3333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88085eafb84a7b527d08501e4bd91e739130284cb53e5a95959be7de722865db`  
		Last Modified: Fri, 12 Jan 2024 10:19:31 GMT  
		Size: 27.0 MB (27021879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ef38c576470c87e83eafa9f55232382a1fbbda87db2d4a5f5dfbaeebff61e58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2986c5fb5d0336d2eff577619854b291e043033313c0b15f54921471faabfc1f`

```dockerfile
```

-	Layers:
	-	`sha256:854c2dcc0c9b9234f6bca82e8e801a27ff65a2569d4faf23431db803c9c20722`  
		Last Modified: Fri, 12 Jan 2024 10:19:30 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f16b48421d7f5442e40d0dbf13aaf2d5fc3663253a79362ff0c838bb75c1d02`  
		Last Modified: Fri, 12 Jan 2024 10:19:30 GMT  
		Size: 18.4 KB (18436 bytes)  
		MIME: application/vnd.in-toto+json
