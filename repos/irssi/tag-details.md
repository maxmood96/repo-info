<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.18`](#irssi1-alpine318)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.18`](#irssi14-alpine318)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.18`](#irssi145-alpine318)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.18`](#irssialpine318)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.18`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.18`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.18`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.18`

```console
$ docker pull irssi@sha256:5030f65c07d60b5f62254827cb2cf9816aeb1acbcd4ae02bf1fc99a047d5f494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:1df930e3dfc77eab0d935627105b60216d5166220605bc404fd1fcef59b28543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18452035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0205c9eb770ca108bf1919df79dc9e7b1ace03abbe7dbcc36dc1103059682d8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56fb333eead475991863177af7e05efd225bc81046ce1b31ce009865c202b9c`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 9.6 MB (9645452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba276003f01fb9916fd0339d39d419a2cfe50878444068526a6db91d04d7191a`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521b358ab5601051bfd274a25423ceac5975a52de10fc96e04aff947b4b65339`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 5.4 MB (5402747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:cb0f81d3545a2b5bdd9e7b7d91dc83b70fffd4606e927d42002f78cf7209f3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3801efd697f47a96b9e94e1ef78afed33bbe572a118a8d715ec30067c6d9b`

```dockerfile
```

-	Layers:
	-	`sha256:f7ce9122a761ceae5f4c31afc898f2295aea2867232ca3b6ef8afd645ffff933`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 1.2 MB (1158728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4180d1dd2e11234c1e22d28c8f1406357b4736bafc0396ddcb8069a33c3ecca7`  
		Last Modified: Fri, 15 Mar 2024 23:54:29 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:f4190f48d8bc546310e5769baa0d37a4f5270b8a97241cb5d8ad6402640777e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17279211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d4da26ea0b59c9960d5fa20c94a391757107fa4808594008649363cd01b733`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5c55bf2b2b99b39993321512092a78553a6ee4a9bc37e759c65e98f2274192`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 8.9 MB (8886456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0c53e61f07860902c9db880cb76bda1dc91ef0c724e3ba8f1a4b65a6ffd277`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43dfaf881ec61aba32b310730d4cf4f102dcf131dca13142b39d5fe17917a65`  
		Last Modified: Mon, 18 Mar 2024 16:02:00 GMT  
		Size: 5.2 MB (5244403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b75cd22953f883341dd3bbdd2b5737546dacda1fd5e0f5c76b65da8b498712a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f24e7b9dc19b8028d020031ac4b5a64261f95e5ec20b106204845391166f8da`

```dockerfile
```

-	Layers:
	-	`sha256:58efe111b310f6e9b0f7cd673ca046d295d6dc8c4dd55241a8f0cb2fa0f52442`  
		Last Modified: Mon, 18 Mar 2024 16:01:59 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:08704e89e8a05605b66fca94a87ee9bc2a55a93fa34cbd681d1627294e92dd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16631167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589cd83606ee17bd1885b4b6062ab226f1988339f3f6f2d8f720682815d8087`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9548c4c0afaf58b9fb40a6053d10180c6b3f16cd2fe65ae815a8afbe710d8e6`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 8.7 MB (8721125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caff03171bcbe4b10ace8974b90573f6672e44d018a7bc6115cedbeec41c8519`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ac0ee0fe968af37fc626412603a726977b8a773a2caf06d22ca9221330f4c`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 5.0 MB (5007357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4e1380e29b9e2ec275f87fafea78d920bf24e21bbcd3659d7c0d3685be0bb8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1178934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef35d7e3f33a8ba2e66339336261e0d460df8a94c8a1eca59cab36b8497c6a`

```dockerfile
```

-	Layers:
	-	`sha256:361b1edd60839d2780fdd4fb58e7d789477a6dcfd7ad4c8be34e24ffc8eca45b`  
		Last Modified: Sat, 16 Mar 2024 16:05:29 GMT  
		Size: 1.2 MB (1161378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a315d709aca269896bdcc95b7f4ee90ac77825e0b993ca494b85d1bab0b30b6`  
		Last Modified: Sat, 16 Mar 2024 16:05:28 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:9f195abd8a7834f6b8651d65171e66dc6d40e83ac06526860a2f991aa8e57af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0d5b53e35edf5d4b671e29ee4434ec9036aaaeb58f1210dd39936c3421329d`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20ad0eea073d81214cf3428a0651c579943a533f8077ef417077606674e1d0a`  
		Last Modified: Sat, 16 Mar 2024 15:24:35 GMT  
		Size: 9.7 MB (9673162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f814c63c2483443b6f20c1b28249c2040e2d82721f4eb99586e3ab1ea91355b`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122530cdfb7d48090e7608c6570ec3b179882f4b1f8e4ae76541716bc4191a91`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 5.3 MB (5309003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1dc0160142db2720e0034e712b2062dbc15a24e85b87e9016d124a8de55424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65f34d6b32adb135b4670e35c9319c44c3a09f5e9b82138788f4cd2260fea51`

```dockerfile
```

-	Layers:
	-	`sha256:32705de4a8475d70834767e07b9d99a55045859a801b23263e5481fbddf1c951`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 1.2 MB (1158747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b47a480b15d4d1783990050fd7bf68c7974032d5d337cda5bd82fcfaa182e2`  
		Last Modified: Sat, 16 Mar 2024 15:24:34 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:53fbd9d62042356cdb1b90f983bc39dd9579ce16d40e7c4583363606d0c0f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a24462b46aa285c4136d3a9650cf70dddf0e0cf9729b78b24c7c2e87e525bcc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978e529ac91378d2576c560c6b43a550539ce99367d86acf89a632f8d1f0c3a5`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 8.9 MB (8904539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477607fbceac2f261be88bbd2cbd97b638d486f65a82ad332f1a42c456e62dd8`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91a8f6d7d261044fb0a75765faa993d792aa0435a5b5598a744b899d6831514`  
		Last Modified: Fri, 15 Mar 2024 23:54:46 GMT  
		Size: 5.4 MB (5412717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:4fd74dc650cb7275ef9dbb486e1c41a0d9dd10ffbf78815e442345791b8caafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48a12d05cb44d8268807dedb2fd560a04b66f253e11b99f9b5dbb97bf095aeb`

```dockerfile
```

-	Layers:
	-	`sha256:d122a1cd2369abd56acc31cd39a35d7c64772dec5faaf53c2d01c3e527ec788e`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 1.2 MB (1158683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82db420fdd01847e4ea7dc4494e85d73fb6bfbc39889bfd07bfc248383d4b83`  
		Last Modified: Fri, 15 Mar 2024 23:54:45 GMT  
		Size: 17.4 KB (17373 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:433de35d2fbfa2c04f5827b168bcccc28e93acfb470beed68c25dae2a8ba261d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18716154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeacfc8a64f289467d32f4d02fa98626c449639b4784d75f058df8a3a37a774`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5c08ce324cea70fc6b0be2547fe5ae48749b2a13e930070db06ff416e86737`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 9.7 MB (9735190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573fefd692c73b2890dcb7f6d0aad394ff65eb5837e91f35140c9dc1dcf31f4c`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e840a820b8d5494706fe52e25b0c81de694312098e9bdad215a9a1e7b2e155`  
		Last Modified: Sat, 16 Mar 2024 10:27:48 GMT  
		Size: 5.6 MB (5631184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:1565b88bd25af151cb32391a803a05bacf9cfc48b9922e35b7e0eccf1ae66a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587ed9cb31d8848a931283a685298aa047931ca15d251b5d08a3c2d2c95bfcc`

```dockerfile
```

-	Layers:
	-	`sha256:280825a1802466a7d2a3997fea0965991a259956c8c1a0a206e8e1d57269a502`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 1.2 MB (1156832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df8399b3a66010145449ad770365d7e7b79ef295725e52502b17f5451317ca3b`  
		Last Modified: Sat, 16 Mar 2024 10:27:47 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:2e66b3da10410535fa7dab9fa887ad0b6f1c12cf747f57fa030829559931561e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18708929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7154ce68bc4cb07c282a740b478508e1d1c9f998c8e149e764af4f4b80115e3b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7a1e7422d5d4a32e8beca36331e463332a216e62e6bfd6b06674601d23f87c`  
		Last Modified: Sun, 17 Mar 2024 22:06:09 GMT  
		Size: 10.1 MB (10082976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1496440b6816e8497e30a2c383b1f0a801c5ae82f1843bab077d9331e6410879`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee92e872e35b961b73cc92e7f8677456004a0e3b21d887daa18091dee87393`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 5.4 MB (5407129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:22a0c93167fe07cd53d1327ddb6dbb3e64592771f6860982e3ad67a23621c138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc6528cb51f659928cb1bea665805ac41797d4ba8150fc6cacd7dbb8679662`

```dockerfile
```

-	Layers:
	-	`sha256:c8929d5af96a0308d70c3244ecc0a9f323d02dc8075a40137b79ceebbf828745`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 1.2 MB (1156774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ee2dc7f1938fce57e421c2a5e880febd71454a8fff8f0208bf1ac084863a2c2`  
		Last Modified: Sun, 17 Mar 2024 22:06:08 GMT  
		Size: 17.3 KB (17266 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:0ceab758111b7494fbe761d554c8ff2c87ee58eee602289e3f6f762a9a7e79f8
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
$ docker pull irssi@sha256:cb52b02b47ba62a45b221465160674688b854b134aeb39f288de72b0d04625c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51992734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f86f9c1407cc7a48b778cd19ea2d4787e4fb3a98364f085bd46053f80299c1`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdc8f1b14a153ff37d57b07d8f61dbcde55d6c13ec6d621e5c3955fe3608394`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 18.3 MB (18267980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf919c5fe11d9667cf12e5e30d470b92bf4562e4761dbcf725c992f82bcb3767`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad42d7cfc543c5f953562e8829ce84e1c66f7c9432efd6ead5dfd0aefce171ab`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 4.6 MB (4590035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2df7eb1800042d1f25d9ed7312d92968be31174a157cb9513dd345f833fc19af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec7c8ce16172926a8897d7169efb1aabe5a18d90320227a9549cd98693c48bb`

```dockerfile
```

-	Layers:
	-	`sha256:7745cc190523f3679c9b2e14d00bc9bcf964b75a9804b253e5fe3de4447a73f8`  
		Last Modified: Wed, 10 Apr 2024 02:54:27 GMT  
		Size: 5.3 MB (5335721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8addbe0c56943825b6400db6d89f3cbd8f74e49779f3eb67835d5bba29180c1a`  
		Last Modified: Wed, 10 Apr 2024 02:54:26 GMT  
		Size: 18.6 KB (18630 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:b29d4bc05b607e7ebf858af9d71ddb6c04988c48fb881b28439e39b704604912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48377853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a67e669125109e37c7a0c0ed5ac15a8da44197cd8af24396751d5d7d9f4c00`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:bfe2e0ed45dd2920845bd9283b7d13266c82fe9f48ba261b6529c28dc246d3e4 in / 
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
	-	`sha256:60d288182f6883c1ed662f82d32316348aac8ca45c943f1093aed5c0ed01b45c`  
		Last Modified: Wed, 10 Apr 2024 00:54:34 GMT  
		Size: 26.9 MB (26890564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ccf16f47c60e6e24ab050fd9023e29bcfa3400078d1faa4222f50f6823224`  
		Last Modified: Wed, 10 Apr 2024 16:28:27 GMT  
		Size: 17.0 MB (17042422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c55720ab88688431305d05ef241a01d72dd03defd4d7acd4418e486bcfa7aea`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476b2992b8a45a93536c383f7f11c55c5b51635da7df926c36d2fd581a64925a`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 4.4 MB (4441507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4793e36e4de433dec4ed9fe33619140731760e15b3d1952a3e1e0388075452f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab412d30842f68b2fe7b1ea7ee9d9a757f75c462cedf9165c366cca183d0ff8`

```dockerfile
```

-	Layers:
	-	`sha256:3ace26e2f59835537b9ac665f8f650fd934b3b013e9b3bba31d95c252cfd9dbc`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 5.3 MB (5337077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85ee483e2c2df2393e8040cc6ea47f38f904768fd3d349d59faed09a4d8807c`  
		Last Modified: Wed, 10 Apr 2024 16:28:26 GMT  
		Size: 18.6 KB (18591 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:01e67a568cf1021282f90b52c54a3dd427b5f7fb9d6900bc2fe9969c18610608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47720598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d612541efeff60c292756af856a7199f319fc6e0929716fe0b61b5f892cf7b81`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
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
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24215226058865cc126e63b32c13e41e8116fe4c2caf22f33f44f0a455bd38e`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 16.6 MB (16635091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2775cbdafa01ee3622f3b6f35fc99749dceffb7761e49a49007ade65a2bb61c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35426ec4c41166c88e92d9e7b8a0dbbd85c58be24b3c857b893df00f22b1246c`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 6.4 MB (6365418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5e0cd66a301c76e49ea0a72176d4477cfe67174d34d2a784f18205e6398c32b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d7ce4724acf26cae6ab52e5f69e1902f749e5eab323e4d838b551315a0fc67`

```dockerfile
```

-	Layers:
	-	`sha256:67a5c2f720a3f66c6f06f6f2c6526de191e4deb78c87d3b95ea70f4f6ea1bfdc`  
		Last Modified: Tue, 09 Apr 2024 07:00:34 GMT  
		Size: 5.3 MB (5337075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cbf045c66d45b88dd784522a41b0697b3f40a2c44742f1c50afd5e471ba9da`  
		Last Modified: Tue, 09 Apr 2024 07:00:33 GMT  
		Size: 18.6 KB (18590 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f078ff734a6e7cb54664d0a537f7b8a68820d2974e7cb42a50ee254fe664acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51710250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381176d60550a82a2145ee28a00935dd8b743441ebb83bd58bab9910da0371a8`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189b844b24fed432b8c02dbf78f0c4526c0e3ba1b73a9088248af38c278afdda`  
		Last Modified: Wed, 10 Apr 2024 16:30:38 GMT  
		Size: 18.0 MB (18036306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5334b8ee73a2f6523639f1f58a2f7dec2d65612186107a70d42afe5606ba6a8`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60333e08b508531dfab1e3480d0c20c13805f55844af37994025093e0e27187`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 4.5 MB (4508429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ebccd2cd038c93acaadf59ffb397f4c7570a96c3967ed9d04fc7454c1935e6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddbd3baeb93d93f2fdb388923ad5b6bf6ee605ffcb12b23f5b6bd3f4681ba8c0`

```dockerfile
```

-	Layers:
	-	`sha256:145444abcaa928d4126db19eef31f92ee1d3c1623fbe89f94093ea4d25bdecfe`  
		Last Modified: Wed, 10 Apr 2024 16:30:37 GMT  
		Size: 5.3 MB (5342118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfaa0d856e23e0c6d386322a16cd0626c26786da2cbb5cfe1abe2d90a550af58`  
		Last Modified: Wed, 10 Apr 2024 16:30:36 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:91aa6f68fece873cd17471650c703a31cc1dfd84ce2c96042bb68d52f376162f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52549610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4724f3987b28db62526f96c9b81c361801314a3160ada7b1935d494c4557848d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3891fca3c98d71d73931d1cec9e9aca1c1f2fb5334c8eee42323a2b9502c6a`  
		Last Modified: Wed, 10 Apr 2024 02:03:16 GMT  
		Size: 17.8 MB (17795433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf5a3410e9851349986c77e3d89ed2d14a40a7736b6b2af76fa9a04fe61e47`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1eecc23b73662df76d61047215171fe68f4624428d136bb4be126084d6045f`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 4.6 MB (4604303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9508405a9640bf3c8d480c28fe8a7db1d13e17248f16a732ba8eb3da7c710078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c94ac5d78b040235b66a9585e9464779b9c1636c0d1cf32ac05c0f449711f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:a63971aa9d8aa083472faa58ad0899f306a07a160d0020b30649e7113fef9c7a`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 5.3 MB (5331799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78dda8c6f51c86671174158e8a7a98b865231801c58e6d5fa234025643aaadd`  
		Last Modified: Wed, 10 Apr 2024 02:03:15 GMT  
		Size: 18.6 KB (18577 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:6fedd47629a1ff84b3ab232269442517c1d720a2354f2168327d6a144222ca3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53577993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d3193506a147f4fcba795cdb927bdc3e3e320919444d391b1b4abf3ddf5202`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:19 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 12 Mar 2024 01:06:23 GMT
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
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfdc178b553f29ffb116c26e468996c5485772b5a27397319069e6d01972b56`  
		Last Modified: Tue, 09 Apr 2024 15:17:04 GMT  
		Size: 16.9 MB (16941747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33deb0a9a1053415325d54ca0afaa4887c2562b01018163556417e8c7b57f3`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41155cc1af360da61c451f6af90bbffb331a38cc1f8d418b6ad18d1a8900ab2`  
		Last Modified: Tue, 09 Apr 2024 15:17:03 GMT  
		Size: 7.5 MB (7513678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:503cc37bb65c75f74908e8681f2cce1452e7355a043958f5bc15b68ca3498ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c25173a31237dc93d00e9af411e6d79a88d40ddde440d5f587b1e67a5d312fc`

```dockerfile
```

-	Layers:
	-	`sha256:6602e55bf9a3007532e717b4030cdb04f786b97250b576aad71186dcc03b1e06`  
		Last Modified: Tue, 09 Apr 2024 15:17:02 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:d148c5c6b7fdfa63232710c32e5c7d7d6c348d3dc36605940190bf09d450c66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56718845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e09dbb8acc0a5eee9d377cb415474bf6aa10264124485d7b3e5dd0b79d3300`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:fd6cd6147fc95a907a092392fe95b8ed685d7ed84c60593cd7e9c64a7d574b64 in / 
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
	-	`sha256:4d891dca051cd29ed554a21d46a9f98401d3ae8b7b85da23513e7b4b1e86008c`  
		Last Modified: Wed, 10 Apr 2024 01:31:08 GMT  
		Size: 33.1 MB (33124837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c547eb0069df0ff04485b510c52d8742766778911d7fe8307a67d063b413860`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 18.8 MB (18765737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a6e424739ff59b6da732b1694c808c59cd7383a92d3c212d494a1a48bc318`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6badf2241aa106491ab5d3c3fe7ea6dbf236008e5cc6d95c76782e55455cd1`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 4.8 MB (4824910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:12cf61d98ee1b795c6a7e94d847ad39fbe48c907bc0eb65188e849257b41f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39197b07e4f3b6b8a495a989735deddbd529d5ad818836dc67458dca156027ef`

```dockerfile
```

-	Layers:
	-	`sha256:e4dec4c908f2ba7f9fbdeb46e83b65174b97ed7768978a3727c4ed3f14e7e1c9`  
		Last Modified: Wed, 10 Apr 2024 19:14:08 GMT  
		Size: 5.3 MB (5343415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b55d7590b1ef07a86a9f94c8db788960557a2a63bca5ed813818a0fe21f74de`  
		Last Modified: Wed, 10 Apr 2024 19:14:07 GMT  
		Size: 18.5 KB (18529 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:83fea55504056b993ea861ab2f91352cf2d661ae8e0cfef5a0d9f6b89b7af96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52778769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd2a2fb34cad67c53d44f55f1b38d9092ed333806959b867c0b58153aed9e26`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 12 Mar 2024 00:54:02 GMT
ADD file:80ab985d4871ca6a72156bedfe1038e6b1a89591fc2fd86c4ef778d293223aff in / 
# Tue, 12 Mar 2024 00:54:03 GMT
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
	-	`sha256:9cada496cd2b8a88571bf23d513e7fce34888d13321fcf23c6613bffe4c37297`  
		Last Modified: Tue, 12 Mar 2024 01:21:14 GMT  
		Size: 27.5 MB (27488684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaa8cd68ea0b2d26f17650aa08357a2d94b9a202fbdcaca2cce84ace0d60e4c`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 18.2 MB (18214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e52dad281c09cd654ed10ad8cf7fb3a2d7b390d4914720128178aa2cbfcf11`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed77cb4c735009b9b6ae9594360ab68daede9ebb34ecf9bded643975c1e251a`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 7.1 MB (7071812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ca4a7a90a6a247c41148f74b4d72c4a4eca54caad921c5d1228a77e4c9286e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2689d0aa1198f887b53734928a2538b39a99b46ed3cc2742c081e743126ad7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eeb688c87115c9f1d2b60c8c7fef64f40cf1db4fda8e5e19fa2f75c7cd6891`  
		Last Modified: Tue, 09 Apr 2024 14:27:55 GMT  
		Size: 5.3 MB (5335022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011b3bc3a58b0fc175ac3e2c33e72998cd79779311e9b225c763cefe5883de13`  
		Last Modified: Tue, 09 Apr 2024 14:27:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json
