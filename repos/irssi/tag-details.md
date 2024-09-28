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
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.20`

```console
$ docker pull irssi@sha256:8433cdf30e274988426352ad38712dc09f28c4c1768569d4588eea8dae437e60
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
$ docker pull irssi@sha256:225eeedb3d5df0d8342c28f28a67e14963a4a3f668754735ab50b36cf23849a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19723767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8718185e934cf00977ac16947769332a38a80ba94b1958d5134cc5096dddec`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c626f109cf0e2e5ee386344e1f4f1278bab9391d09e043d3f9afe609c04387`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 10.2 MB (10191821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e1b9dda433c6260ec07e1572c0120eeb2205ad32293eae47eaa0a81b43bfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fa96080be04b7162785b53e6197cf44a7906954d44de78eb0bbeb69eeac92e`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 5.9 MB (5907140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:187222cb890ac3b3f65f968a23c8375217deb65302025ca80d3bddd34aa6405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ad74886f316acc6cfaebde6ff77de40ec17fd0107308bfb57973256f59e8d5`

```dockerfile
```

-	Layers:
	-	`sha256:f7ca62c1d6b0082fb2d26f943a081038469132453899545953a91012cd4e7375`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 1.2 MB (1180425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77417a1071ef7e7085c110ce17cfa06c18b50cf1b1caf8ba006a14f926abb21`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v6

```console
$ docker pull irssi@sha256:bc876fda49849676e70afc23dfc3e74c36da0c2a3745f5fd3c28a8aa9b8635b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18480137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0c54c34c514e6637fbbdc3209d255343b87c65ed581f951673640306e1dac6`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4563366942775996dc7eff42d60df711ef73b0fbafbca9edb8d797024668c202`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 9.4 MB (9362097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b0c6e5c33e41b06fde0292dae092dc763b7e27b823ab7be705407c11384bd`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcce1db33190250448077f9d4cd391b9ef2b6a67f7d2fa94f27bc0362e4894cd`  
		Last Modified: Sat, 07 Sep 2024 02:40:26 GMT  
		Size: 5.8 MB (5750537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:4d1617b7ab5430803bbd52362c57bb453d8dd4acaedf8bdde2447432a7ff9e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a999001bf9c39d625593692a3b737f6f3a0b814b3c4811047346af7fada502`

```dockerfile
```

-	Layers:
	-	`sha256:818f414539c29d70896c89b3932576101e8e18ce58a90487359afb4f38d44f5b`  
		Last Modified: Sat, 07 Sep 2024 02:40:25 GMT  
		Size: 17.2 KB (17221 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm variant v7

```console
$ docker pull irssi@sha256:1d02a8ed391c51bde9b27afde1ea4240cc487cf74dbf61e5d2efba692b2799f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17782449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053a71b3a279ad0e3a2e0d7dbbf4e54ad2278be015c7f288b5fd103a4d67c754`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0429f3169f57cf771d30f0b785f6c7a5ab02d43411f8d6f2344100a482351a48`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 9.2 MB (9183709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5dba3974eab46837cadb17dfa4a364e5da3b9bd43af9186c06744a8fd58a40`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255b010ec76769301234a17a2d0bdd32e205d39407d7962c89e1a5c79b89851`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 5.5 MB (5502241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:14f64ac5066b5ca789c86b0625abe3210bf749b295085d8d92dd6af200205bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1200797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32f9747e49a5665b3336fd605ddcdacc76f8ada3a5d544863246fb41d31ad24`

```dockerfile
```

-	Layers:
	-	`sha256:35094785d6853a5f0461474df37f8127ad609827a2b89f696d94a63f97125283`  
		Last Modified: Sat, 07 Sep 2024 02:57:54 GMT  
		Size: 1.2 MB (1183357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d31524ff73face1950830eab2bd0ed7ec05e4012f74641a1b5a49010fc1998`  
		Last Modified: Sat, 07 Sep 2024 02:57:53 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:62e8dceafa5dcc45ea2419d86401fbf0824b7a4bae684d174ad74b52a78abf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20053478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec1e645d1e32a1d6e4842461b9a9b6b03670618d7c7be7a3c59a8f9773ddd02`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad68fd7a6bae4d6a9f0791e9a8b0d89515ef68cc3b3bc2802082159c8f0b917`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 10.2 MB (10157951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1759a5bf2c0e097fe22b543d149e5fdcd014e7b5f039a9fdb8b9ba503d6be7f`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0df7ac6458b3449bfc8746487857687df8de1d04144326f711d143f904e0da`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 5.8 MB (5806884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:964aec0691615b07c0f7cf64bd3c2aaf8e77f54ae96bd8ae41c132aa2d21c32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1198193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846e8bd16a6800d33a45be72816781d99d14770119347a9b650981b6cf2073e`

```dockerfile
```

-	Layers:
	-	`sha256:fe65408852799879429a8939ccc5713fad8538db3615fa77035290c4b582c5ec`  
		Last Modified: Sat, 07 Sep 2024 05:27:56 GMT  
		Size: 1.2 MB (1180529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d76afdd382391f2e7f0b7e5e52a8af475ce69ab9742ec727e6e0d04ed084114`  
		Last Modified: Sat, 07 Sep 2024 05:27:55 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; 386

```console
$ docker pull irssi@sha256:cec60383cb2114de36cc450b24a795c8b842ea3fe2b5d3ae261777966088981c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19101566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f9750cde5e598eddb25cb06de3196c475dfe940267f34c736aeebf2d606696`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fe8a84f82ad300ce90efce39dd06078babce03103f8b8fe54cdbafb1fbc1f5`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 9.6 MB (9637197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d066bbdeb2014769a48d8148c61e03de10dbfb7acd1ab85f2ded1e7fc00d4d`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264d62ad1faa811627d0ed73c1b84f1ac7d0eb79bc1dfe11cf881039971566`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 6.0 MB (5994206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:8fa447d248e4470c90876cde43ba4113beae83308c1df0897cc7ef9aadc43c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1197639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e42131d18a25107b03a2c3896713f456d13455b6ae6538165e7722393cb301d`

```dockerfile
```

-	Layers:
	-	`sha256:9e6c0cce7fb0dd7e8aa2edbf38f26a85728a617a5dd3a52ad2b45f225e21aa48`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 1.2 MB (1180380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9529db747d4db3bf62950ed172f88b0bc2940614e0ca337601c634c09ba51f2`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 17.3 KB (17259 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; ppc64le

```console
$ docker pull irssi@sha256:f4295c16c15be6d6b002444faf906a4376f6a034f0fb10e7804ca1a0eb5a5d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.1 MB (20117357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612e050904415a82d96b010cd7125b10f3b535d204678ca2a9de0dfdd94b5bab`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7f01d0ac0592b557f92ad27859bdcd34b46bd87f3357c86c81131ba4c1ac3`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 10.4 MB (10379021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e046fbadf0eb3f861ca076d737a51e9d3f8f54cf0fe5a50fd781332a42914a3`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 967.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e93d1891687db40bc621f9c7c4b32ada1170a9c98951f1fe4aa315a844c730`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 6.2 MB (6164918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:ec763bbab32c460ad03421366a5aebc14cf613d6d45bb177fd44d671e3bd6371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5a8fced4a91a234e459d3e86f70f0a875ef57ce7b3b2778200d6692f8cc1`

```dockerfile
```

-	Layers:
	-	`sha256:2121fb019fff014bbc612a435b5e0209feb68478ca72db18ce1d8ca584be271f`  
		Last Modified: Sat, 07 Sep 2024 07:03:06 GMT  
		Size: 1.2 MB (1178529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52d086952a00b69d128df0a14d1bdc11dfbe5c91859e833208040720b9d0efd`  
		Last Modified: Sat, 07 Sep 2024 07:03:05 GMT  
		Size: 17.4 KB (17382 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; riscv64

```console
$ docker pull irssi@sha256:856c91783f7d21012b38323b36991a4b415b148dcab362efe6d45ca221b9d692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18948633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b8fdcf190add01c2dc00e479ba691543a23c72901c9b9581734e8ecbd4d80`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634141d08a7f2ae5a144da1847d931b4cc99514263aea51e764b222d536642bd`  
		Last Modified: Sat, 07 Sep 2024 20:33:42 GMT  
		Size: 9.6 MB (9645875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8a2a2ecd95ddd7ef0c9d83f432abab63b16ead3200fd2df5617cfd5b8f0e99`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49e9fc5ff805842d79b092fb62541e430a9fdb5d1144f8a360cc2fc1171a61e`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 5.9 MB (5930308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:3acf8b9addc44a281e26766672e6142aacb88117e08fb56734b09449033a5a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e863619e8a6d2f0955b1b8e1da7b02f294d705f526e5815a8d990aa430482ab2`

```dockerfile
```

-	Layers:
	-	`sha256:00b2eeaffa4b740f8aa8985162c83d7a26da17ff5e9c3bd70b0c62d8dc64788b`  
		Last Modified: Sat, 07 Sep 2024 20:33:41 GMT  
		Size: 1.2 MB (1178525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3f803218dcbba5730579592f427070a871dd2311ce2e2ceb98ac94e033cdb3`  
		Last Modified: Sat, 07 Sep 2024 20:33:40 GMT  
		Size: 17.4 KB (17377 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.20` - linux; s390x

```console
$ docker pull irssi@sha256:a9343811b921bf367edda23179c3a2567bc8c35339371a584986716c967d30fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20273410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:386a4347853f194ac5a1aec08dc721a00fb5214f62aa6b5619bb97822cf8d8d7`
-	Default Command: `["irssi"]`

```dockerfile
# Wed, 22 May 2024 22:40:32 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 22:40:32 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf007dfb739e6f45d5915a24bdaa5a2d439dd6e0b3b795852fdee75463ada95`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 10.8 MB (10753338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21af45072b07676ab768b93ba8bdbd6ea9039d1a189f72d756aef2f352d7f0af`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 966.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6f5d317148da6283d176e25e9078d039f9c168bb182f7d79b401a047fa5c44`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 6.1 MB (6057476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.20` - unknown; unknown

```console
$ docker pull irssi@sha256:c64fc2803cf39d52ca243caa6b69e23565bd37c6db576f2956d712bee758f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1195787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e5d62029e06315a1f9d7c42efab99910196d2f0539c13839c2644d7722b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:fa51fb87e83eeb4a26311a4273a680a426aad645be1a2b2166305da4793c83bc`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 1.2 MB (1178471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc9bd2b4610dbaf8c034897233371f6d76f0932f7276e254755a2a774162f786`  
		Last Modified: Sat, 07 Sep 2024 02:48:12 GMT  
		Size: 17.3 KB (17316 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:af8fb1e34382fe8bad3f828bb30f1da0b53f83bd54e1d716ed14fbcba356df8d
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
$ docker pull irssi@sha256:6f531a45cf9570796f490ca7fa53af33a5cd4c0ca575013cd7be472ab76fff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcffd11b71c7300aa1978d6d57887b9b6523efd8986a4dfce40e0fb503c6c4ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28db2084d8bf4407b88b69cf8338ee753036789ea09a80f9043cf3dc6cd56e7`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 18.3 MB (18268760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9f0fbd3fabe6f5a9d6f010f3866c1e8cf6d511587ad597727fe191ae6dedf3`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bece764890ab5ea64f9e66078df2d092c063c16280abc11cc837f24471a11ab3`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 4.6 MB (4592813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0522a64ea0213a784b6db17a508d6b990b763dace9705a60bc378a60dc6962c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8545a05d8029df0eb340e6f78160a2f85369fa1144792eae86b42003b528554a`

```dockerfile
```

-	Layers:
	-	`sha256:4cbb7168423b841d357a99852505732a7fc1d388c4d16e2b563de7a9729addf0`  
		Last Modified: Fri, 27 Sep 2024 06:02:24 GMT  
		Size: 5.4 MB (5365679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29b5a7e1b5cf85504a1335f42c88a7ab238d742bae92f4d72640c6e90abd7f0`  
		Last Modified: Fri, 27 Sep 2024 06:02:23 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:3fc2179e0c13515c5087909c5d6393a5d2fff8fb71aad7db7d6a97de76d6e215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48374610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad98dfd893071fba7e821bc94cccd3ac92924c7e60a44f6d443fc8384314af85`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
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
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4016544bf1a1dbe70de06ef6916c244139884496c00d49b9ef493d1e93e5e78`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 17.0 MB (17039418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80c37a23f1cb348e605ed68d744bccb0a781c23f5e0aa75c5316e2e5c02a3de`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcad8212a94a217fee9e4a470b35d03afbd9839cbd4a243680ac0c5b92ba0f3`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 4.4 MB (4444532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:79d232f1a78fb569a891f25cf3f0301da727a7c501edfe689c4dce34854e0364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712deb8d3cac183d2957acc991ef2a309bc19ddc88092aa2beb54b5761f6af6b`

```dockerfile
```

-	Layers:
	-	`sha256:c4ebf815dde70879e8e7a407172dc1df4f71aeef4d053b801a00ae4a8cb5c0e6`  
		Last Modified: Fri, 27 Sep 2024 10:41:57 GMT  
		Size: 5.4 MB (5367178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34a893e6825297c52135374577b3d51a05907f03c59e613393d2c3b34584756c`  
		Last Modified: Fri, 27 Sep 2024 10:41:56 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d1c4032a216f2ccccf0c7b284a2ae44b08352485c92a090a903048f70590eb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d66cdb0893584321106efd85f7badc6d6ff20c48d1e3af7988491f84f4c9569`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e563c3399a8aa736a4eeeeb01a0fc0b45b7378e1bdbee518f59153f080e8757`  
		Last Modified: Fri, 27 Sep 2024 11:05:16 GMT  
		Size: 16.6 MB (16634318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320631944547615451871022669142675cb9982121c3e9d83f0493359c70793`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29857a57ce61e1eae53c5287b9a4b1af3b30519fa1b1d5b28093d4ad0aefb27`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 4.3 MB (4299023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:03153a6500ea5c6b8fffcfd39bd06b8bfb084c4160b70170353fe2a38de8d0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5385677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba56d0e94dcb3ba6ec0bed841e124b16ed3aaf1ed129ebe011ceed0d5e22f20c`

```dockerfile
```

-	Layers:
	-	`sha256:8f98657982e7227f68a1935aa22016cbc36962bb370e0b1724d231d771afe091`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 5.4 MB (5367033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5f4071fca1b69cd94fa3e4634dc6c2a83c74d29bc6cc68779825cbe86ad01`  
		Last Modified: Fri, 27 Sep 2024 11:05:15 GMT  
		Size: 18.6 KB (18644 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9b8063026b72b3218456063ff744ac962ec1743ca1c6a204e4c6a4a503f28eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51721074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cca46c0086b640160f4dfa56275a5819f62ca7ec39c12fdbe25de2bb0fbe3e6`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a960fa2760230ce2a6287d7e37d8bcdb9d83a3ad1879171d29bacf3ba093676`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 18.0 MB (18048277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435e3c638c1368e810ff6ddaf27efd271b8ab54a02207feb5848baa822dd0ff`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97aabfa9022e1fe9f564b4fc4671fc6a3063e0f9b622cafd514c7371e3c44d7`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 4.5 MB (4513070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:cd8051568919920c6e07854d16b1c249f4296914599f7325506b4c85dc9fcc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487f423b634214280bfc9643f2eea1ace7fb02c85dd11111af1f6cc9ff1a2203`

```dockerfile
```

-	Layers:
	-	`sha256:763c24fe39c2c3bb1e4f2fbf6f1d31df1a40c79c994f916b6f193869f32a0a26`  
		Last Modified: Fri, 27 Sep 2024 15:10:19 GMT  
		Size: 5.4 MB (5372161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da8e570801e0fc1e7886e3f0d742a13de2f289695e62f569ea9c5b253865c8a`  
		Last Modified: Fri, 27 Sep 2024 15:10:18 GMT  
		Size: 18.9 KB (18873 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:35fb45fbcd064f25df75320a8377bf6188c2be939bf677f675a0a280568c2010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52561786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70be6b1f75a30d6b62a1cfe24a3ef45a0e3c35e43b575a021f7076b9fc99cca`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e74527cbcb09c234dda4bb19536ede39dc0ccbef8375d80f0a0d507dcda8e4`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 17.8 MB (17807580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730d24c35827e30762a7ee1cba1c418aae64713f60a4da06f44e24cb5e9f2ca2`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf5d42413deaf55f7ea40c88e81c583ebb97de2e653f2c1344c1dce18e50020`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 4.6 MB (4606635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:75c7165494df6ca0c8f84ff96e11ca44fde23bcb3e30cccdd1f217517eeb515f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5380219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3235b29f401533471c5e09770ed85ca22b16e79855590835e981b26562c28d`

```dockerfile
```

-	Layers:
	-	`sha256:ecbf6b7f62c44f1d0642ace00aa439e2d70a9ee81d8f8f85e42ecc67709c396b`  
		Last Modified: Fri, 27 Sep 2024 09:02:28 GMT  
		Size: 5.4 MB (5361757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab32763e60b82d439ad4b72781104072c422e0b5db0d0a1e4dc4f4e2a7564309`  
		Last Modified: Fri, 27 Sep 2024 09:02:27 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:291d87011c5c636d069d6f74c6796c03d2208d050713b23db2a301c6a54bc9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50633180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e6aa70a891ce32f5488c0353e6f02facfb108db6ba13dfb255a05038802c24`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d53fbf788bd0e7b28f97c4dc927f8ab5bc32596e4d316d1e4107d63df122e3`  
		Last Modified: Fri, 27 Sep 2024 23:25:12 GMT  
		Size: 16.9 MB (16949902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2858574a09072d459734ac302f8784ee2119cd1028b5d0e81359d03e7693743`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86aa9a6bf5e9b33a0ce592db709ac8916b028b333caa0bbdb8fba1bd2f6214cd`  
		Last Modified: Fri, 27 Sep 2024 23:25:11 GMT  
		Size: 4.6 MB (4555066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7b17417d51f41d70cde36d9d968c36209ddd5246b2e9a87b8841b2c1aaee76fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd0d67639923b725e3575a86ab49679b4125e46a54d6d4697146278f381a88`

```dockerfile
```

-	Layers:
	-	`sha256:55950ecb6cc8539508cfd44c53f5ad3fe2fb065c30a19cc098db41c8cf9a68da`  
		Last Modified: Fri, 27 Sep 2024 23:25:10 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:f1de57552259a00cff771c947f62ba0b1ca9bb067621004699a4a9bc17d6dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56730548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba165270ef39e153dea24de7b197a7df528e8e67ba0954086364720ad64c394`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf583d910d0cea2b55e4364dc8201fd6ddd1ea4ec589349a547c585f4e495b`  
		Last Modified: Fri, 27 Sep 2024 20:00:18 GMT  
		Size: 18.8 MB (18776219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e4534a2ddd3b324656add8cda05e54dd226e723cd92667319eba22fac3a212`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5f561dffeee4ed0f0c5c238405b7f832542ed8146797a764d15d81af016786`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 4.8 MB (4828806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:b272722b7ef214e7d94ca783ff9026882118d6c49e8dac2046c79afb25772658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b19a667e27ce859ef7ae97ae4588868c57b3e12d23ab6c8cc8365d15c1e9351`

```dockerfile
```

-	Layers:
	-	`sha256:4e772231a6f0b350cfe05456a4ff1c7ab736eeaba346871934dd56e3193eb082`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 5.4 MB (5373373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8c322d6e3ffbea32a4df5dff9116c4bbb4c6cf2b058e98fad345e9a2d0e19c`  
		Last Modified: Fri, 27 Sep 2024 20:00:17 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:0db0ed2abed8f2dbdcb5e955930f10c55b829d55104ad5c7a4770dd0b2a90a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50307967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e414a3c884d933b1ea8fc0cb788b9078429684e55defdbbc9fedf4af6a2dfab4`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfd107efe55ed93bcce320083143eba16d25a9b229771ba6cc4d0b9f9cb8757`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 18.2 MB (18227901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970a0a58efc4f46fd9fc42fa27fccdfbe91ca3b06e1867b690e5d16394fb5974`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c6ffc75c120357f8f5ae3e3fc9512df539c003983ba9b8392bf189612efbb0`  
		Last Modified: Fri, 27 Sep 2024 13:10:37 GMT  
		Size: 4.6 MB (4586685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:81c205063a86057fc358ba52f208a238f04cc6fe699ef10b35ea023448f19066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5383496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1d062126b5b44aa63480f09187e398adf936e75160ee754740ed78f618c682`

```dockerfile
```

-	Layers:
	-	`sha256:7f5b21c36c68722ba80768d3023fce3837204713314b0d4f24eb87ee29002c95`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 5.4 MB (5364980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d848af853dc7dda657d634b7d51f1980f448edf338b200ce7d29aef1a4578f2e`  
		Last Modified: Fri, 27 Sep 2024 13:10:36 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json
