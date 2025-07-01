<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.22`](#irssi1-alpine322)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.22`](#irssi14-alpine322)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.22`](#irssi145-alpine322)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.22`](#irssialpine322)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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

### `irssi:1-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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

### `irssi:1.4-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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

### `irssi:1.4.5-alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.22`

```console
$ docker pull irssi@sha256:c6911e509552d6ceb7a1d1765803e4ccf4e57ac93b92582f3cc32ef1f94e0d39
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

### `irssi:alpine3.22` - linux; amd64

```console
$ docker pull irssi@sha256:50936253f7e9bea3065af16edcd345429c3de6c0037b25a4697d536c88fe602d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1d38e76ed4f47da2e26f47da3b28a3275970e112b0129a842d480e03ba1661`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bba1e6a0207f1bc842ecaacb76769918e667bd76769cb32d423d7ec7bf6ae16`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 10.4 MB (10395382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b172497e163718f6bd62fba80547c0f5525813755aa92204caae16a18b322`  
		Last Modified: Tue, 03 Jun 2025 15:03:12 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82932d8b2c4fa18bb168beebaea601ced2dfec6f377cbfbfcb7d4caca34b2cf4`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 6.0 MB (5973851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:46132c981929f742d56c67d7d39205d6e2c9e85cc6e1a157ee035ef47be679d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301269c81f4a418e424c13ca3c6a7508e6ce912f59ac1a9001dd50c74f9539d`

```dockerfile
```

-	Layers:
	-	`sha256:d5141c19d7d7c29ee96ad3455a6b880b48c3d23d580691e98ed9466098bd560c`  
		Last Modified: Sun, 08 Jun 2025 15:33:12 GMT  
		Size: 1.3 MB (1272597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183b20b2db8baf1730ae6d210cba41c1c79d4e59162b64e831cc212eb1955ab`  
		Last Modified: Sun, 08 Jun 2025 15:33:13 GMT  
		Size: 17.5 KB (17543 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v6

```console
$ docker pull irssi@sha256:00606be5f5c499237ef667ce1c80eb36c1eb156dac2536d3bafa41aef3b43ef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18926133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217977963fa09f47fe049e58a26c6b3450359c70699d6b566ad5c4182881d54d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3153248a4a7850a727a5d6f26e82fb349adeded467d74118725447ee6a267d2`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 9.6 MB (9622034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a17f1b3942390d02e1b736b20b690693c5373ab96c4a8fa4002495dc479b0d`  
		Last Modified: Fri, 13 Jun 2025 09:48:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a397351f1e24e9e6fc9afc41663f6f47503fb0f71a07576b03ab2d9b646358`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 5.8 MB (5802184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:4ad32a599623b35c607c0d909b378c1da41464673cd2fe1c236fe6148e6b2367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb31e2548acce52a030a611a0984f06817204dfbb64a174642d7d3f7ca8a3f6`

```dockerfile
```

-	Layers:
	-	`sha256:118a93dca8b28bf155d355531ea143525b3e996ca9656e3f6862784af5d94f34`  
		Last Modified: Fri, 30 May 2025 22:57:30 GMT  
		Size: 17.5 KB (17458 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm variant v7

```console
$ docker pull irssi@sha256:cc42226d345d0b51964f45cbbe1e75ec5c39016cf8e35b071d23d0bed7f429cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18232907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6934e67d3108ef5f857d789f522d4eff760c8cf18c747754e78724ac2a1d5f`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0921b3c12c0ebb760049a51a6b241c68931d21acf0a9773af2a01e3abf7b80`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 9.4 MB (9449953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f65363880d538a6f0aaa2b58898331af0cff042dfdb6f8c9dd0162e4ba1e1ef`  
		Last Modified: Sat, 07 Jun 2025 08:15:41 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffd667d038e18aa5a4d1f85ef1b26da641275ae2a979ad1634961ef6ca37fe`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 5.6 MB (5562786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:896c21c381e31375b8af6d14c3524e027616dbf23f53e92a580f859e083a621a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1293327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882b9288bd08f8e0f10df833b810dc3c58f0edf0c83b497ac81d955420bd7622`

```dockerfile
```

-	Layers:
	-	`sha256:7a8a9d96500197123083534e346d523758241bcb15fb3e50f919457d3215e481`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 1.3 MB (1275655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0540212a67c76c02006b54064c9cfe36ea040843783d23069280678729f435d`  
		Last Modified: Fri, 30 May 2025 22:57:19 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f9e5cbb13c38711b5896086fe26433b4d29d0504fed711c26757956326196bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20340650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93efd351c0b6cb78978e539b7c237cca04c2da2015c858dc56e399e5f79c226b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c20f8c499ea56d3f68ba44b10d2a1bd64592dd78ae92d529250c23f7ec5752`  
		Last Modified: Sat, 07 Jun 2025 14:40:33 GMT  
		Size: 10.4 MB (10356164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9232c2c988a3f17720d946b4ba801624609114719e6878e63bcd45946144463f`  
		Last Modified: Sat, 07 Jun 2025 14:40:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce727d73355eeb82054f4df93607dc965ac719adb682dc537c5676610663625`  
		Last Modified: Sat, 07 Jun 2025 14:40:41 GMT  
		Size: 5.8 MB (5847558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:6af55f1628e4b1c29a438b0831130ae124aafe595b3d192dacddd5a20f95ef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb5f0fafe6f9fda0a0caf8330aa3775eae7e4f053c87500f1d4313269e086c9`

```dockerfile
```

-	Layers:
	-	`sha256:d9d17ce5c6da6ac690630e30c29a86c9ba55c554935185645a4f90ac29259a80`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 1.3 MB (1272701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601b09e2f13666292daae2e456bcde7f474f1793ee082b7ea884355ff366b77c`  
		Last Modified: Fri, 30 May 2025 22:57:25 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; 386

```console
$ docker pull irssi@sha256:4a17d99139261e6616ed676d600732aaad7dc09aeaa79255a20c19fba2eeccd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19611630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254e972cd07cc37bf7d5d17b92b69ed8ab8b6b583cb415156eb674ec0845410e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58dea6c4d3918e041552724e9bc3fc86609864827890457063e2e8ec579a3c2`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 9.9 MB (9938949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e81feb958347b9c2062c7bba52a6df488101843acc857bc201e49a23003c4fb`  
		Last Modified: Sat, 07 Jun 2025 08:02:49 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b985f65d394fa72217032d96820383482d34079e28d44ab18b5dbaedd323c175`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 6.1 MB (6055666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1264af9a70e3a320286f3aff28d43503cfb8352c54317d2f881450c1152c5f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1290035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29296ebb20b4f69238a6ce7b61e0d6919dc7a976df04a2e9ee51ee42f0f99968`

```dockerfile
```

-	Layers:
	-	`sha256:96d9328bf243e69dd2bb3ab17a0a4453f9267885fa02a9f818591e690dcf6c94`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 1.3 MB (1272552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fce96368b710458e1106a8ba9a198545be09baf039b97bac1384bd3c43e4dc3`  
		Last Modified: Fri, 30 May 2025 22:58:19 GMT  
		Size: 17.5 KB (17483 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; ppc64le

```console
$ docker pull irssi@sha256:d45f3c497fb522fbe08a5d374b1133539a02fa94cf88d62818d8beb928a73f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20558018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3dd3786454813a1e3e6e00be4e076c13a099035f123204b8c4ad1241b6c61e`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bba03f8e7e1b63a1fa4ad3abcc23bd147c4503d8d4347b3db2a785b46b8c5ae`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 10.6 MB (10595337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6699f6fe809c6b3605660a34f66a3d1a1d473343e279d5c196c268166fcd166`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49bfe08c7d8f1f8a8de68333e3ee6f26d2260dffb986bf525dab0d6559752f5`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 6.2 MB (6231507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:186f34435148516d6277982269dcc7d523210d5f192bbf65666a35f46d021598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212635f6e235a0a6f0737c337de16e88f1f08be4573f352f0ee30aa049e4ef1a`

```dockerfile
```

-	Layers:
	-	`sha256:d89ec3f7f401c316a83305ce0f172c30fdc65f7ff873ec0cd17a5cfbf4488a68`  
		Last Modified: Fri, 30 May 2025 22:57:49 GMT  
		Size: 1.3 MB (1270704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73c79fb8bf457aa3b1ca90d9c09e5a49043d2e40e4d867206c91069f8ffab19a`  
		Last Modified: Fri, 30 May 2025 22:57:48 GMT  
		Size: 17.6 KB (17615 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; riscv64

```console
$ docker pull irssi@sha256:e83d00fcfd0ab1ad17c13d868ce4a82ef2a1e29e17e13dcf3d734a7d9bc3d098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19338006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a59a310116ea166b9919a45ad320034bbd432965228fdfe21e52136b2429d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79ce9cec043098f97ecad069665b27fdf966800bd7c00bec7b9a4ea01b3c377`  
		Last Modified: Fri, 30 May 2025 23:02:56 GMT  
		Size: 9.8 MB (9838394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e7eacf22686a7571dee54aea423eca89c1e9332d27e62150f2e46085fdf651`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7512ce4e7a8916bc76565a0309706c5f20772446fb5b0f463dcc1087ba437a57`  
		Last Modified: Fri, 30 May 2025 23:02:55 GMT  
		Size: 6.0 MB (5984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:1fc458a88f48d4fa227cd88eb997b45cffca58db1f04cc25174a309da7281db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4747e0d8527d071ab66cedfb04520544adf7aa329833a456bd593eb8ad296d`

```dockerfile
```

-	Layers:
	-	`sha256:8711fe32ebd0d77d80927c9d51adec7977c914334e7b0190fd6c1971c52059a0`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 1.3 MB (1270700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94aeb09fadc69a8522a28948fa6fd83ad3dc5b6fad76b7831f3253c1cf9b5e51`  
		Last Modified: Fri, 30 May 2025 23:02:54 GMT  
		Size: 17.6 KB (17611 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.22` - linux; s390x

```console
$ docker pull irssi@sha256:caadef1ad33345e9552717319d2a3bfca37a43e1f508d733f664a78cf6326c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20730813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d52bb07aaafffcc6595392c321191578f1fd1f2f1cab4e88a0d541df2666062`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:14:55 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV HOME=/home/user
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 30 May 2025 21:14:55 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:14:55 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 30 May 2025 21:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Fri, 30 May 2025 21:14:55 GMT
WORKDIR /home/user
# Fri, 30 May 2025 21:14:55 GMT
USER user
# Fri, 30 May 2025 21:14:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0339d76e1427af215b88308c7f9e672afa57e16edb00d717dc8892172493a0fb`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 11.0 MB (10957611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de17d3f971764dd79e529eac2a08294d68fed90429215dfc47aba8388d1c0780`  
		Last Modified: Fri, 13 Jun 2025 09:48:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa15a0ae763bf81b277006f20c870e0c630c8f436fb1b01737183ad4722a98`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 6.1 MB (6124687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.22` - unknown; unknown

```console
$ docker pull irssi@sha256:05e933490606758bb325546d22e78f29e8ee3dd40a9e03e26d446e67f29af903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b8a8232854d512d4c64852a4f447cdb763d4d2c4500ac477008276f6efc67e`

```dockerfile
```

-	Layers:
	-	`sha256:393676de4c0ca86f78450b45bef2a48fa06cd81b30e152d3c25c323b1c1ec271`  
		Last Modified: Fri, 30 May 2025 22:57:46 GMT  
		Size: 1.3 MB (1270646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b4d970204e7f7db21d3f11c4fc53c1fc7db3e28c817f4593fa66b65e3781d0`  
		Last Modified: Fri, 30 May 2025 22:57:45 GMT  
		Size: 17.5 KB (17540 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:aa739be735f83873499c36593645d8f40848c7d254b61068c24feac71b05f16a
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
$ docker pull irssi@sha256:2cf74b146eb20d0a786822ddb4ef7f40203798e758118233f4ccbca678fd7ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51063206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edddf868535677204c5a7d28e3cd9f918ca046b0050726b3197a5d26e0b3dcb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57696dd1f4b6f1f7efeb6752d7a80bb66ae467c773bd2562e7a9928f0c282c44`  
		Last Modified: Tue, 01 Jul 2025 02:13:12 GMT  
		Size: 18.2 MB (18236940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae555c7b4028931c40d00bb7e2b2df23217a9bd6a3acd7aef015edaf20a4d63b`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7e7caf5716f9a8d2e5d567f9eddccd9c185f9db428e3a37553d0a88bd6f87`  
		Last Modified: Tue, 01 Jul 2025 02:13:11 GMT  
		Size: 4.6 MB (4592767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:33f6cc46ada596a7ba3d9e2487870476272da7be1b12adf46680601ff484defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5560036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4a3fe59dcaa298024debd5d2679986855481b9191d45299542ec45b17fbf`

```dockerfile
```

-	Layers:
	-	`sha256:d8781938a4c4f6985e9c72d1cf52a4f120e22aef5e312e0cf654de976e5976d8`  
		Last Modified: Tue, 01 Jul 2025 04:59:40 GMT  
		Size: 5.5 MB (5541320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46c8b16251ee7c9db9c7aaf17775e1a51a425755f03e4edbf96f104947cfe106`  
		Last Modified: Tue, 01 Jul 2025 04:59:41 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:eb829e61b8ec9486d5a3bd7ee33334a907ea01eb6ebb045e96d61dc5b437528b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47230934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d1dc5067c2dda8bfca4fc03a784f463815099e7a15b551a9d5c6dc140132f3`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
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
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04b27175d0207e3f2a1d1306c9b56f17cd26cc52f3ded230bb415a5415ba9b2`  
		Last Modified: Tue, 01 Jul 2025 02:25:15 GMT  
		Size: 17.0 MB (17020413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6597ad0c6ae200d96b69675a2d11e1afca99073cf04bf33f1309ee07a71710`  
		Last Modified: Tue, 01 Jul 2025 02:25:11 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac2720265df1d1c796bd2568b9de391a67f2248c3863f9e0aa3939b3649a4c`  
		Last Modified: Tue, 01 Jul 2025 02:25:14 GMT  
		Size: 4.4 MB (4444708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:859315da7c36c471ed1f841d68a0f3a3ae1e27a62add8e52e883dc7906a65fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5562087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2024e844dbac4dc38f743120c9a170064959e26635be185c0eecc63b3fc80d1`

```dockerfile
```

-	Layers:
	-	`sha256:76d3827bd9adfb3ce84f3a4d75e9c14990077cf5d4e20b5b4f6f473f5d1b6d8d`  
		Last Modified: Tue, 01 Jul 2025 04:59:46 GMT  
		Size: 5.5 MB (5543237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34daf291baab6a320078ce34e8f2cf19f73409e0669b2690d7a645da4a1b93c`  
		Last Modified: Tue, 01 Jul 2025 04:59:47 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:7ce7ba9e357617196015433ab4842333aae9041c13700adacd8b460586f91b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44848190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19a43ae7891c28120fa9587f691c84681d65b81bc7795df2087b3c992fe78a7`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
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
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9177b0ec76aa8d0a391119fa755b019362255a6b0288d01ec4742b3770f7f2`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 16.6 MB (16606957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d82ed46321fffc470c4117b1fbf85208e416f3b22021d10d0c457655b56fe`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a548007ccf10e75a2958b08b9d5a854fe5d6b43300b2796baf7f2cba5090d`  
		Last Modified: Tue, 01 Jul 2025 02:28:15 GMT  
		Size: 4.3 MB (4299133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e589bf6c14ad3ff3a2e7cdace865455a6fddee82f436c2a0b12d2b36b2f99277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b8d06c6d2c240363a0ef37885bb3f585a1dd98144584cfe782dfbcaf3e79f`

```dockerfile
```

-	Layers:
	-	`sha256:5f5df57dd9de82b403de5a415db0c93795f75165f4066224026f48e78be4c1ba`  
		Last Modified: Tue, 01 Jul 2025 04:59:52 GMT  
		Size: 5.5 MB (5542678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62704b96b4163695906895ed6f72bb5ef0debd8686697c04be425c920b2a8fa`  
		Last Modified: Tue, 01 Jul 2025 04:59:53 GMT  
		Size: 18.9 KB (18850 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:2b4401070933f94fec804b08723598167b4954489c3799672574eb6614d7bef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50606844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78adbc941e2ecbfe8e037c43b878a4bfd33aef60c8530ed5050670acb4cbccf`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41164d3d01a7c735e6fafecc467626a5c77671ce8a0fa33911937eceb8c38ddd`  
		Last Modified: Tue, 01 Jul 2025 02:59:12 GMT  
		Size: 18.0 MB (18012869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c288378b9518626cb677b03f875f3a279e9b3e1d3af9a4f7e6481758a8d790a1`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc2884b724db5249d0aad9500cebc9751483a3ac83b2e275d8f184d2b254ede`  
		Last Modified: Tue, 01 Jul 2025 02:59:09 GMT  
		Size: 4.5 MB (4512941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4668b89432bb1f15378c5b36370bbeb723a0a51915a16e751bcd77e63e1e928c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5566693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5f99c57a4120af2a9905abde28d181bfcab8c8f17dae023399f20741caf3d8`

```dockerfile
```

-	Layers:
	-	`sha256:524fc05e8c55d957ff31e66ef6a5b859943d347b177bd2fd895f05e6b32dd142`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 5.5 MB (5547796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12def9da49abaf40dbc1b26bcf18e573d48b05b9b74c7bd55dd3e42562eccf10`  
		Last Modified: Tue, 01 Jul 2025 04:59:58 GMT  
		Size: 18.9 KB (18897 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:841ce10a555a4196723218d763161d39be9aa991784e1461f2b2d1089fc5a6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51588308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d60e4107a0f1e04a16943f7a540afd943b36fc3c190fd23fd146690fc0b46b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
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
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db64584438752d82a9b1a3659ee66e1250d822e318c4165e2e7156632020ae92`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 17.8 MB (17765828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aaad2c9d37fd64940abdb0cf1b139975df6b2a986bd8005c0c8827c059f4a3e`  
		Last Modified: Tue, 01 Jul 2025 02:13:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf72bfc9f4fe9beb9c5fd045cf186c726d7e8249fb500819fb07f8488fe5bf4`  
		Last Modified: Tue, 01 Jul 2025 02:13:08 GMT  
		Size: 4.6 MB (4606685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ca0a6fdb7b32ad63613764b3ce001b53c6c02d73238ac3a0b2aea93f3c363402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34d1694f0740b3d00db09ad67db91197fe2a373db58aaac29e1a569d3c767b5`

```dockerfile
```

-	Layers:
	-	`sha256:5a105a85d6e0a4052e3e4f8228c89561b05d2b9e7260b7f6f3d55a364609acc0`  
		Last Modified: Tue, 01 Jul 2025 05:00:05 GMT  
		Size: 5.5 MB (5537453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbe9e806407d30fc47200ab051bc025d9afbccd0dc66869c7447e57dee57829`  
		Last Modified: Tue, 01 Jul 2025 05:00:06 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:df5967c9ede98973f92ca74da7b9845e59664590055eda3936fff81ea857f853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49988889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc6ab6ec0f553393d02077553022cf3ffc5a846e325cb49eec1ab0a0cf73f6c`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3296150b7b262494f809274cf6020339620c08ef1d168b011a96b76a4696f6`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 16.9 MB (16913919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91276b554fdd588689b56c518ac2a15d919bb634f6a22ee6229b73e5b4ef0045`  
		Last Modified: Tue, 01 Jul 2025 03:13:54 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23f1b6e68adab84bd82f90d3851f6c031bacd4d02f66bbe971adad8f1646307`  
		Last Modified: Tue, 01 Jul 2025 03:13:55 GMT  
		Size: 4.6 MB (4554875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:7efc3b11581765846c9e124eb7be12d006ee89f759e8a60ce008344e39b6f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.6 KB (18608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45946433731fbf58bfb2b4867c99c0ebff3d4bbd3ffc3696a628ff3efd8f9a7`

```dockerfile
```

-	Layers:
	-	`sha256:28afaa65760b79b0c61460fc55fb38d9071cd20a154f175d12689933306f6744`  
		Last Modified: Tue, 01 Jul 2025 05:00:11 GMT  
		Size: 18.6 KB (18608 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:d7db3672adde7499dd8af37789772056af438e8abe23246337adb4d73717f67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55629197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0688eda7c5408dd2a546f6993425c437e3be9f32aa2983f700993f5f39f8fe8b`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d742a1b12e4e5a0f841e50a1d0eb563ecdb21579abe63655ed98339109a965d`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 18.7 MB (18724035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d8d0f8b0828926b123bfc747c086e2a1881718364a41f1270482420e8af31`  
		Last Modified: Tue, 01 Jul 2025 02:30:35 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60cb0716164153511293bb6b417aacb8aecf53d258875f56448b5f5404798`  
		Last Modified: Tue, 01 Jul 2025 02:30:36 GMT  
		Size: 4.8 MB (4828986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c51496f462044314008b4bafb301aa6237b00791c9adfdd4de262aeb3c6084af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5567922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf88cba7f474f45a0cbbb4ea3aebdac4c43c036398d83ec0148515e0abf1cc3`

```dockerfile
```

-	Layers:
	-	`sha256:b200921713979cc7ceaa1d7383cd12b785c182e0b33090d2bc87a16529acad0d`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 5.5 MB (5549134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df20cb41db61ef18d9c5b8d1a6611b712c4a9d412967cea0cbf5a0b4e8da25b0`  
		Last Modified: Tue, 01 Jul 2025 05:00:15 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:eb6c645f0cc9f7c270b33d1ae81e1a7c9e0e74ac7c3e205baf75cbb642c58b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49677972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c2f9f3238b98a44b84739e43f5598b382680e76f7fa8ec5a7535b438cb3fae`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc79993540ba198d282b4b42d2e0de5963f9b7daa15c1cffe3229d4f7cfdce`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 18.2 MB (18200122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21b44156ae87ed7d82e3dee6bcc308edf8b42d6068b34ae58aea1fa5212597a`  
		Last Modified: Tue, 01 Jul 2025 02:25:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67968054f3832c8af6ec21841af3ce496ce9b6dd010826cf433ef481068a8b7`  
		Last Modified: Tue, 01 Jul 2025 02:25:38 GMT  
		Size: 4.6 MB (4586682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5fcfc176d1b6d40b147206774627a8fe9bff068bc53c031c3bfc2782bf325d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93284d538a2c3cc2bc3d96e4d5b0e22aeefcd88fd28296baf2412b88318a4f02`

```dockerfile
```

-	Layers:
	-	`sha256:63f01ce8bf78615b1a6305fd1e0a0477bb3399b2d634e6c0620fc6302d15317c`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 5.5 MB (5537622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b39ba887c39429b1a7213fd368025ca74111de20205aea2241eb6eacc22681`  
		Last Modified: Tue, 01 Jul 2025 05:00:21 GMT  
		Size: 18.7 KB (18716 bytes)  
		MIME: application/vnd.in-toto+json
