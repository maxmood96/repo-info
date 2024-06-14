<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.20`](#irssi1-alpine320)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.20`](#irssi14-alpine320)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.20`](#irssi145-alpine320)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.20`](#irssialpine320)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.20`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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

### `irssi:1-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.20`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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

### `irssi:1.4-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.20`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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

### `irssi:1.4.5-alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.20`

```console
$ docker pull irssi@sha256:54638695015b5e6e60213a6a1b1ad810ea7f846ede5eda1f0fe93b4bb65cf0d3
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

### `irssi:alpine3.20` - linux; amd64

```console
$ docker pull irssi@sha256:6f1026b1194e3c6d217e9ba8d81d6d73cd10dfdd997a71a3539cc26621842efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19724252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26c2d32716c942b836ab06f5d4c3c4ce60e9c908da2585f3390bcb8082337ff`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef207a375de35e52f9478e60da8509621a78c41bba74f78edab95d787b9b4d9`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 10.2 MB (10194048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c40618ed2f8c8385f273fe05e48b85555e1c0c1e090967436194534da6b9dde`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86621e6bb9d68992c598318898dfc50b26a3845a31c2d77ab0d686ac5eb06b`  
		Last Modified: Fri, 24 May 2024 00:54:52 GMT  
		Size: 5.9 MB (5907114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:20902744e69c57bf0f6370d4e8ba0a8d28c150073cd31ed3ab34fb35511cbbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb601bf065e6503465f7091b2f4f58216e74dd76df56b5e334191c3a9baae7f`

```dockerfile
```

-	Layers:
	-	`sha256:2fc57191849b00717f828a6bbf922a0e8b0ad0179fef7bac541a0283cd7a3221`  
		Last Modified: Fri, 24 May 2024 00:54:51 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:60ccb65e12d38d7eb073b4e5bdd25645c45c09aadf833a2ee51db8940d49ade3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7ee42385bab9042610c01b1db8d5b7e27b655d40f577818f69c297885e17a`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7fcf5f584f647910537bfc7ff03b48e112939e4a907f3e7a7d2682911e2a4f`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 9.4 MB (9362057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18e5cb996abab40d7c9e6c764fca0f36cafd08c3ab21c4c21d06e55c72924c4`  
		Last Modified: Wed, 29 May 2024 00:00:49 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c88b1cd851466bf438264e70fecd31c3956db5bcf6d6920f7fc29114987cbf`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 5.8 MB (5750368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:bfa31fc3e742a4d1560ff201bb8f16aeddc0edd0f8411d0a01720c3f11bdb0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46955520be46d925ce55617fdcda8c46192be6b74c5cbc2b8fc5509d76bc042`

```dockerfile
```

-	Layers:
	-	`sha256:b3419fcea7f5369802b18f60e5274c4b424631eab43392f272b13a9e5cffbcb3`  
		Last Modified: Wed, 29 May 2024 00:00:50 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d0ff7bb186641d1b22d3e5d22c39f75f71b233d18e1396ff4a37e811b3e6039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78345e4b0594384a4fcb079602614aa641c6789ce38bb762197cbc5d1035e561`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f6c5891b79fe2ca346b2ced6ca8aee3f290f3b28c5aa6d642d75127cbffb1`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 9.2 MB (9185710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651f730a30a6516923d9b8c6d8f058f2ac8630ba445d7462a1682660732c698`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5949dfa91c9ebc23d466e62a9c4b4cb51390e3724b50070276138670050345e8`  
		Last Modified: Wed, 29 May 2024 01:18:53 GMT  
		Size: 5.5 MB (5502132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5ba8ffc21a5b464a8f5efd3528b45745752dd339229dd1a44d775a067fc3d6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a899e29492c0c082822677f1aacb789df9c4164d0249ccb67d8f3f3ee4df553`

```dockerfile
```

-	Layers:
	-	`sha256:02144cd3f252f069887414ea371af434e120f2359108978a3fb514d2f19898a8`  
		Last Modified: Wed, 29 May 2024 01:18:52 GMT  
		Size: 17.2 KB (17172 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:673d0b2c226a8c966b02476af4c851ec002d76a762af91c48ae075194b75ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e170ca1ef05d2e9a6b47b68fb6bed30137907b2dfef59abb6520a66c3dc2e01`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033e21cee9e3bffdce816b6f56af120215f4b750220f25c8f6195557d2bb8f1a`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 10.2 MB (10159282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35972ce859a30d11bd56258d900b5396ee3aafaa98378e2a402bcf4bd206811e`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6031dbba8fc9017c7ce3f7ecb633e2e051bd19dfd9f798342674d76763ebd86f`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 5.8 MB (5806109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:1cdcb706ba30b09bdf36bf1874cd033c47acbe19f8c054a500a050aa32d172f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708ecddbfa2db35ec0dafd3af1a25d505a15eec12fde665664924c36c23c9d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8e1e242fb3d18fdaa46be5a7980413738454008ac2a4e1421a1668bd0461ecc9`  
		Last Modified: Fri, 24 May 2024 02:48:33 GMT  
		Size: 17.1 KB (17066 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:12ddec451718ecbf2bde0ec74a9f082d852a1071560e84c353c9337ad3f2aa78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19098234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5020fcd949ffca9b4b3090bd02d4e95bebb78b8abffc05a952bc8fb11ef592`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9edc66ad047e2ef859aab279817bb27236b58aeb6939d18eaa1d0b5ec3deeae`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 9.6 MB (9636387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219772d9899db0610d906e35df391a89067f768427b72f77c9628fc4f95eaddb`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1c1f9c384002f71f8a088486ec5c8a1915831625f03ef499c30e8023297ab6`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 6.0 MB (5993670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:5f0f81971361bd0e82d1712071abab6d984c31374226d2c8437cf9b7cf8aae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d439aa0119e7cd5ca235d64e7c458cafe8f8c4564a9bc59ba35a546492a2e777`

```dockerfile
```

-	Layers:
	-	`sha256:7632b63494e83217ebf57f014f15ef791c0b6c2b7408a7bf95e186ee82fd9de9`  
		Last Modified: Fri, 24 May 2024 00:54:43 GMT  
		Size: 17.2 KB (17157 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:8e927eefec09a3cfe65974fb6e0b8f0f081f3821c4620f62c4f84ee4db3dd736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20115172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1af9579187d537ec2098799827ac52af2e9508d8b2002aa2fd79c813651d08`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2493b16f76544faa556c02064ed1b62fced58356ec3f474b0a4c3c916d30242`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 10.4 MB (10379405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e4f8346529ff16963ea272c12a9a4299f299ca6991778ce0ebdf5ccd7813bf`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc627e95f5345f0c74684747c5e3a17b2ab63d0ae500dec07f6718fca576164`  
		Last Modified: Tue, 28 May 2024 23:07:25 GMT  
		Size: 6.2 MB (6164922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:639da9cf4ee67758e8856edcfc1a8e3c27a1d69a495306f6dbf92443d94832d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1a50f6e93bef209c4bb40de6f0f949456e692d70f84398fd30a9cbfd2a847`

```dockerfile
```

-	Layers:
	-	`sha256:9db9ddcba64bb2d38c83eba22a60f23cde4bb252913946cbf4aa5cb99b5b252c`  
		Last Modified: Tue, 28 May 2024 23:07:24 GMT  
		Size: 17.1 KB (17114 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:2065a951e2f5130eb8c45368386d4b7c062b4aab9ec3c9b3da130575886ef86d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18947189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a4707b4eb2618a4f0e5e589d6fbb343aa545bfcad75f607712eb682a929c6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00afb65e3acef31fb7c080acc0e765e2e9b1686838ac6dcfd649e3b81557e4b`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 9.6 MB (9647594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa4ef68cd8ea0f64a2efb1e7187266e9c1a6f34b136ae88e0072a17a1a0ffd`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 968.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12e67dc140ed3c237982c2f8ccdf291cc8715d30952ac9ad74c0a519363bca5`  
		Last Modified: Wed, 29 May 2024 21:29:27 GMT  
		Size: 5.9 MB (5930035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:d4e28b635de942f3ceb821bae32cd36dc765c963599dd791d2e99e789fcb7b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 KB (17109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d55a2aa611a1c42aed6c2bb3bf2685f905101d86419dc9fa32a4812b91904`

```dockerfile
```

-	Layers:
	-	`sha256:d7f1691f89fdb2fc94079a3c8cfd527fcc105cc6e34ec41777021e5a4c673900`  
		Last Modified: Wed, 29 May 2024 21:29:25 GMT  
		Size: 17.1 KB (17109 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:3091e86d3b67109e2b21ba378c8dd3be20b28756de579d6b20cb6d43522fb9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20274016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6231344af580079196d643f2c9e96e939daaa481278b6ea827d6e2c0a6a3557`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 22:40:32 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV HOME=/home/user
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Wed, 22 May 2024 22:40:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 22:40:32 GMT
ENV IRSSI_VERSION=1.4.5
# Wed, 22 May 2024 22:40:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Wed, 22 May 2024 22:40:32 GMT
WORKDIR /home/user
# Wed, 22 May 2024 22:40:32 GMT
USER user
# Wed, 22 May 2024 22:40:32 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13736cc92e9357a5f95bde9bb83e9a0a0c485a923debc27e5fa391ed8d38651`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 10.8 MB (10755517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e1c83fa55bf04d576c29f7eb7c6ae9815b3b0cc3fe7b1468d9b08fe6a5df7`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72900a66ae8163c57913f84694ad57fe169744b2db7b69c36e2aca2f54fc9b`  
		Last Modified: Fri, 24 May 2024 02:07:08 GMT  
		Size: 6.1 MB (6057162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:00e509c2a2ff2473a1056331029d1c0fa377954ed9c05fc87ffd8fa6537c7860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 KB (17048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cc780e962f2572809c4f3382e2aff3f361e96985617cf94334b02abca0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:8c5429b23d12503e53db9a16d3626ee02cd1b60ead08e0696477abc80a4409da`  
		Last Modified: Fri, 24 May 2024 02:07:07 GMT  
		Size: 17.0 KB (17048 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:3bb3d1a9d12c916d4a573ede34f87b2e76f665aff0107f99a60fe53704138a12
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
$ docker pull irssi@sha256:c8ffad008f2fd9cf05967dec8f3be7448224ac29eea70e0c5eb5136fd9372af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51822834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc02aa55f106f34420cca6f573205f8cadfc92d5ca97a8abc4818c8d40e79804`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5605049ba5bea20dadcffe83948c4089a7f0e2913cc181991797bfaf7ce1693`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.1 MB (18076130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee253e53d79dc74d4493983e977168de727381984a3f76821cb5cc96126c68c6`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed71768f8fe19e3ca54499e6898d033a805dfec7e1db92ae8e9d62d7130ea36`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 4.6 MB (4592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0fd955f91f0a9bd0521a6a1f3ea234b608b50dbb2340b34f6634d806b8bb08e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877df2e76651653af2fc99ecace950baf962a56463382b9b80f1e6d2a04754e0`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a1515f0daa4476fe873fffd3ba9f24ab38a6b23c8dfe8a5d8bffb279bf753`  
		Last Modified: Thu, 13 Jun 2024 18:29:09 GMT  
		Size: 18.3 KB (18297 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:5f725c2e5d2ac9727969c8ae4954a70ef6083f9f3898e622bf1f4863e92f5079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48210866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb5ee9a6b959765edcc05e16fe6621b4590bfa3ac6a086c8e82e2c07c5cfcea`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9784b56b8034452a4f44a324089a9593b49264af2c7c926a3e2b0bd223249beb`  
		Last Modified: Thu, 13 Jun 2024 15:25:01 GMT  
		Size: 16.9 MB (16853096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ae90cbe3568785414d3922691d2b03a842428113ea167dd4207fcb1f43e13b`  
		Last Modified: Thu, 13 Jun 2024 15:24:59 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e243381a003d2df8730de42a4177a24e9992ad42f69b49c53f418f556b68ce7b`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 4.4 MB (4444440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:50ee9a986d07b30761eec1da47a32df701b7c68664a7332a5a8afb33bd57561f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96a30386d7f6ebe5e40a01095c2e03065b44c9000956bfa1692a82e5a84eb0`

```dockerfile
```

-	Layers:
	-	`sha256:c592c4638c25866428197353d1635fadb232853a0e96a7b9661011fe527d6328`  
		Last Modified: Thu, 13 Jun 2024 15:25:00 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:dc6dbbf9ce014172f80efb37d4ba2ba827e3628ab00f6f8917df17df4c2c7a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52378101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6dca1188ccf28b1c56d87d6279ec8c52bf2166a7aaf14059443feb98d9ac5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9566639770621f217cd786db72f56fc9ed72118b187ca1d68ee3dc1f6264b465`  
		Last Modified: Thu, 13 Jun 2024 02:04:45 GMT  
		Size: 17.6 MB (17605531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc193101186bbfda154491fa4cc0c5298e4071a7c7ae13d0480adb579904f27`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ef20f290f4896482ba4c50481b647a8732d3e249bc565c3d75358b9f2af8e9`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 4.6 MB (4606556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:93b4e202e949c53c5a1219b00343a3df411162a8a5ffca4a639709c402ad2e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72999de3a1af31b0b72e76337e057bfc3ba31fc90d899e3ac6319a6b6552bc31`

```dockerfile
```

-	Layers:
	-	`sha256:ac24811e0ba633f66faf4865790f3531ff1b47900e9a5cdae7267e6d2b2527e6`  
		Last Modified: Thu, 13 Jun 2024 02:04:44 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:6473780ca19c8cf014be2fbf1ee024731afa78aa235b8a65356f4d1c76408ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56547350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a98ddfd285fec54f8f743e21cdc4a282c6faae70a31ba7bc77b52c16a3c4f55`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede47540197b124a606ebead423c203319f34d11580485fea860829d4b5a4f62`  
		Last Modified: Fri, 14 Jun 2024 00:39:22 GMT  
		Size: 18.6 MB (18574100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835143700b7cf2465336e6f3130d29c4f12f7e116617f7eb2d19ce74c1af019c`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4c27c0e286fae61369113cb937126a57a5a9a58445905d87901c35381ccb`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 4.8 MB (4828699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ae93710262af4ee5a889e98340551d1e0359e9b010461dbd6d4ba9c7fe2afe70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87c9ebdf833bf8de2b47444c69f51564f4cb7b569eaa3bedd1dcc191eef2930`

```dockerfile
```

-	Layers:
	-	`sha256:96156bb9d5b72a38c66d9f8c867c3f4288d5f3471d7d0f3c409d477c3d51701a`  
		Last Modified: Fri, 14 Jun 2024 00:39:21 GMT  
		Size: 18.4 KB (18363 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:0b4cf56d9fd337207d67cd60b8d72ffa80252c739f9f592c574fc125b9986763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50125964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de7f66112c6f5bfd641061ca9cf26c8eae316c9420e81a11bd8226970576381`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
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
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c89b98d6e43f608ad2f6b61103d718b4b65bed068ec895f4d69b2eba242c94`  
		Last Modified: Thu, 13 Jun 2024 09:40:32 GMT  
		Size: 18.0 MB (18023470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3447eb51aa0dc3167296c6ba4aee475d9d4f16a33f6c2da3477fac1ec513920d`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80b0f3178151fcc6351c61a8805f6ef0e3bfda542d147100abd708206ff38b`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 4.6 MB (4586676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7fb181d2f5eac98b8fb51d8892e4111e687e4c680031c27fa89f889357d40fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89591c0114bc40fa3b8906bacea29c9818260727d48f18a0d15d1caf327c8348`

```dockerfile
```

-	Layers:
	-	`sha256:fe5f77ae730e4cd27a7552f204b2bfaa0602f42ab437941c7b130c9bf12c866f`  
		Last Modified: Thu, 13 Jun 2024 09:40:31 GMT  
		Size: 18.3 KB (18296 bytes)  
		MIME: application/vnd.in-toto+json
