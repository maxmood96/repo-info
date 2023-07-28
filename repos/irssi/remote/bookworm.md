## `irssi:bookworm`

```console
$ docker pull irssi@sha256:a66e6db33868043d1d308111fe9d4884f83ab43a5c6c3198c5ba32a99cfcd437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `irssi:bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:be5b179abcaadb228348751cb872428449c05d7c0fa94df8f2dee51e271f4e80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76048813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7649344d5fc9d159070ee195a0662e35256ed15d03b19c30ec90597bbf460485`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:44 GMT
ADD file:209589a8bdb5a3788ee42ecdbccbbb561835dab96b0d8286bb5a2229d2f41be7 in / 
# Thu, 27 Jul 2023 23:24:45 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 04:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 04:06:40 GMT
ENV HOME=/home/user
# Fri, 28 Jul 2023 04:06:40 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 28 Jul 2023 04:06:40 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 04:06:40 GMT
ENV IRSSI_VERSION=1.4.4
# Fri, 28 Jul 2023 04:07:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Fri, 28 Jul 2023 04:07:18 GMT
WORKDIR /home/user
# Fri, 28 Jul 2023 04:07:18 GMT
USER user
# Fri, 28 Jul 2023 04:07:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:648e0aadf75ac2ef63c5390adc6dc14fde37a5ad88c2870ea604df0a9c0eb4e5`  
		Last Modified: Thu, 27 Jul 2023 23:29:26 GMT  
		Size: 29.1 MB (29124532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc18848ce2f7955ad37b2560db048d468e810fc5d1cb1177137140166534d2e`  
		Last Modified: Fri, 28 Jul 2023 04:07:43 GMT  
		Size: 18.2 MB (18242760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cb61fc63c5635f06999025d0d0716e23b4ab1fed5ce7e299e8c32873e9ac84`  
		Last Modified: Fri, 28 Jul 2023 04:07:39 GMT  
		Size: 3.4 KB (3373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572f0fd88000ca27e164aecbb1951cf2322cc60bf95243601cc14cfe71e7ee05`  
		Last Modified: Fri, 28 Jul 2023 04:07:44 GMT  
		Size: 28.7 MB (28678148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:aec78e16d10718c1efda2959c1b8aee947100ebb90545de6e08334aa621c9d6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70392251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ad0ec605ca4a62cf214ba2aaf0b26ad706593a6c59b9c1519c0eedccd74ccd`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 04 Jul 2023 00:48:31 GMT
ADD file:ff5b6029e7e4f2b427f101b31a8dd8d15a3a1204bf9b0576e65270de33ea2f62 in / 
# Tue, 04 Jul 2023 00:48:32 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 12:52:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 12:52:35 GMT
ENV HOME=/home/user
# Tue, 04 Jul 2023 12:52:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 04 Jul 2023 12:52:36 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 12:52:36 GMT
ENV IRSSI_VERSION=1.4.4
# Tue, 04 Jul 2023 12:53:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 04 Jul 2023 12:53:28 GMT
WORKDIR /home/user
# Tue, 04 Jul 2023 12:53:28 GMT
USER user
# Tue, 04 Jul 2023 12:53:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:da4ec93bf9d039ea6c48e256f41d88db6aed3ac72074f4cffb3f0c1b41ccac78`  
		Last Modified: Tue, 04 Jul 2023 00:51:54 GMT  
		Size: 27.0 MB (26982160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca56d725a0a921019ba95976abe2d122616ce42038b29438e7ad4f184c84bf9`  
		Last Modified: Tue, 04 Jul 2023 12:53:55 GMT  
		Size: 17.1 MB (17083322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad1da099e214287a1666642053501ab6fe4081e0d57daef02ae28f3eda329b`  
		Last Modified: Tue, 04 Jul 2023 12:53:50 GMT  
		Size: 3.4 KB (3369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d9f402cc0bfcfda121c1295e133a554a5b9376645941bfbc5792445f92200`  
		Last Modified: Tue, 04 Jul 2023 12:53:56 GMT  
		Size: 26.3 MB (26323400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:65cc24a66952a2cd4624c1189a160c6b82681777cdda6a7c7f917e4eeb41ca96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66703842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a986bc604c274b04bbd599316a542a00ebc0e9bcd7fc279061666320614b63`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 27 Jul 2023 23:57:46 GMT
ADD file:b23161e9856801127e0136a920bcf075410ac23de605c82ca91d285b9f35941c in / 
# Thu, 27 Jul 2023 23:57:47 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:49:34 GMT
ENV HOME=/home/user
# Fri, 28 Jul 2023 03:49:35 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 28 Jul 2023 03:49:35 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 03:49:35 GMT
ENV IRSSI_VERSION=1.4.4
# Fri, 28 Jul 2023 03:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Fri, 28 Jul 2023 03:50:10 GMT
WORKDIR /home/user
# Fri, 28 Jul 2023 03:50:10 GMT
USER user
# Fri, 28 Jul 2023 03:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bb5b735234291ca6f672f489206ea5b6354d358f7d75a05036bdf84a6858d9f9`  
		Last Modified: Fri, 28 Jul 2023 00:03:11 GMT  
		Size: 24.8 MB (24805329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb6dea8c1a1726f27b358bf8fd36e55cfb92ef58b438008ec539528d51b6980`  
		Last Modified: Fri, 28 Jul 2023 03:50:30 GMT  
		Size: 16.7 MB (16675096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61e7bb2876eef16334596a4a3259695f9f8688d0e672409228a0de2bd2ad3c6`  
		Last Modified: Fri, 28 Jul 2023 03:50:26 GMT  
		Size: 3.4 KB (3374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00b1d03a3bfc78fc571cddcca583748e0d23c38dc92ea014f56d2edc6729563`  
		Last Modified: Fri, 28 Jul 2023 03:50:31 GMT  
		Size: 25.2 MB (25220043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:d1d6cde5e5c2a999e9152d4364ae5be83519f279b0d591697e56e423fac1675e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74823643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e0e91a857f6fb4affb2f5344acc94e7c908d8af32b0ad2a3f4cae9a4f1b57a`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:00 GMT
ADD file:1de2ba0dc88aa343332814e19adc6b850d08e62c31589fe902b8eb2cb465934e in / 
# Thu, 27 Jul 2023 23:43:00 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:40:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 03:40:11 GMT
ENV HOME=/home/user
# Fri, 28 Jul 2023 03:40:11 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 28 Jul 2023 03:40:11 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 03:40:12 GMT
ENV IRSSI_VERSION=1.4.4
# Fri, 28 Jul 2023 03:40:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Fri, 28 Jul 2023 03:40:43 GMT
WORKDIR /home/user
# Fri, 28 Jul 2023 03:40:43 GMT
USER user
# Fri, 28 Jul 2023 03:40:43 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:90524f7dc01b4ce9b387992acc6cbdbcc2a9ee8c6addfd632429ca06ea18751e`  
		Last Modified: Thu, 27 Jul 2023 23:46:17 GMT  
		Size: 29.2 MB (29157226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb48eef9562a02a0e2b42b4c9016c6c9ec7ba21ad1fb6f3c255637a1754b2dd3`  
		Last Modified: Fri, 28 Jul 2023 03:41:00 GMT  
		Size: 18.0 MB (18024793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afe3d652adf61e1935db1078738d3f0e67ed54be52bb9291a82c04cf2009b15`  
		Last Modified: Fri, 28 Jul 2023 03:40:57 GMT  
		Size: 3.4 KB (3375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be06b8351ce60f5c8d840967f37b56a8309763e71541b1d52e33b0a7a27a0fc`  
		Last Modified: Fri, 28 Jul 2023 03:41:01 GMT  
		Size: 27.6 MB (27638249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:c240382f35c52ff4b85df05add38fc552e0b126872bc27c44fb2ac3b4ad8abc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76490482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f227a1c808ed2762c09bbac351cee3b10fe7ce2c5fddf4ef5bf8b1996498697`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 04 Jul 2023 01:38:36 GMT
ADD file:441addef37edd5da10ca045fe9cc7863b0785f468d83c3884456efd567e97536 in / 
# Tue, 04 Jul 2023 01:38:36 GMT
CMD ["bash"]
# Wed, 05 Jul 2023 01:36:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Jul 2023 01:36:59 GMT
ENV HOME=/home/user
# Wed, 05 Jul 2023 01:37:00 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Wed, 05 Jul 2023 01:37:00 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jul 2023 01:37:00 GMT
ENV IRSSI_VERSION=1.4.4
# Wed, 05 Jul 2023 01:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Wed, 05 Jul 2023 01:37:55 GMT
WORKDIR /home/user
# Wed, 05 Jul 2023 01:37:55 GMT
USER user
# Wed, 05 Jul 2023 01:37:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d4b098d102e200415126181e2b6aae752738430f2ed6a601f84baf29e2f7d01`  
		Last Modified: Tue, 04 Jul 2023 01:43:28 GMT  
		Size: 30.1 MB (30140746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ab165aaa197a8deac894c79140cff60a9392d9d3529cb49fccc689e218b40`  
		Last Modified: Wed, 05 Jul 2023 01:38:19 GMT  
		Size: 17.8 MB (17783887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccfa18f731e557051a3c6082f9d9a27b112de0a1b0ea6581e79d0a5d7a6cd60`  
		Last Modified: Wed, 05 Jul 2023 01:38:13 GMT  
		Size: 3.4 KB (3368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab31a94a2f5365c16fc532833a97e510a0883dc16825f720fa9d46a554eb5ed`  
		Last Modified: Wed, 05 Jul 2023 01:38:20 GMT  
		Size: 28.6 MB (28562481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:540cb1c9a26b8e74c3409a44a7d9ff73b4da9447957c3faf5332f02943664a00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74058250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:848c38189774b5caa1cac536f0ca697c6401e7e43b5b49d073c7eabe74a54d83`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 27 Jul 2023 23:11:23 GMT
ADD file:90cbcf9a2aaf48a433b00118dd0821eeb291092da7b7f67ce6a525ce2cba1e3f in / 
# Thu, 27 Jul 2023 23:11:27 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 01:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 01:40:25 GMT
ENV HOME=/home/user
# Fri, 28 Jul 2023 01:40:31 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 28 Jul 2023 01:40:34 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 01:40:38 GMT
ENV IRSSI_VERSION=1.4.4
# Fri, 28 Jul 2023 01:44:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Fri, 28 Jul 2023 01:44:20 GMT
WORKDIR /home/user
# Fri, 28 Jul 2023 01:44:24 GMT
USER user
# Fri, 28 Jul 2023 01:44:28 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:3252778e08fa8eb67ab052ad63281284b5ef1afdc40a36021228133487ab5d52`  
		Last Modified: Thu, 27 Jul 2023 23:22:26 GMT  
		Size: 29.1 MB (29121405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d92d0999e4e4a9dca6d717d83687b6a4560745c3b10805f9bb46d3671afd289`  
		Last Modified: Fri, 28 Jul 2023 01:45:08 GMT  
		Size: 16.9 MB (16925209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a65e6ce6b543f71d2efcaae0ec6e13787e30f68e7ec18798759a22497bdf2f`  
		Last Modified: Fri, 28 Jul 2023 01:44:52 GMT  
		Size: 3.3 KB (3297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8aeb0dd664a15241433c6f8b98abaa2c1d58754dbe49d2c0568ccc194b7882`  
		Last Modified: Fri, 28 Jul 2023 01:45:14 GMT  
		Size: 28.0 MB (28008339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:808102c091e0f450e9fd0ff09dd607c235a6972c0982e8a909041d95ecdc9bb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82057404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6db42123514bb5bb81836bd52afbea22d1c59d575a9cf77f3cf7c9ada892240`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 04 Jul 2023 01:17:51 GMT
ADD file:51887002f5002ccc662adbc6ecf1129e3db375a7a77b93da43cc9a8326b3c4b9 in / 
# Tue, 04 Jul 2023 01:17:53 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:36:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 06:36:17 GMT
ENV HOME=/home/user
# Tue, 04 Jul 2023 06:36:19 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Tue, 04 Jul 2023 06:36:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 06:36:20 GMT
ENV IRSSI_VERSION=1.4.4
# Tue, 04 Jul 2023 06:38:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Tue, 04 Jul 2023 06:38:43 GMT
WORKDIR /home/user
# Tue, 04 Jul 2023 06:38:43 GMT
USER user
# Tue, 04 Jul 2023 06:38:44 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ba99a1aa5a92d949d988e66df7723a542fd81bc30eef9d4269e8a899820d4bb2`  
		Last Modified: Tue, 04 Jul 2023 01:24:36 GMT  
		Size: 33.1 MB (33116716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a472629dc3d35e78fd046fa9c53281082c6b5a3cbf7f446fdcd3c04302e339`  
		Last Modified: Tue, 04 Jul 2023 06:39:27 GMT  
		Size: 18.8 MB (18754069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd7eaa97c83385d341b2e6b1823b9021baeb70ce87fcc47e593bff57983efce`  
		Last Modified: Tue, 04 Jul 2023 06:39:20 GMT  
		Size: 3.4 KB (3370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bc505f4c9f16e57c14adb02d3910e21d2031362fc3775c1f499928e77048f2`  
		Last Modified: Tue, 04 Jul 2023 06:39:29 GMT  
		Size: 30.2 MB (30183249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:bd4f3ca68b2f92da6f80b7a88bd32dbe63219753a81a621764bbec4790ec0055
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72926978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfdb66b346658a866749a2daae4e17bb23270c191f1443965d707963ede1abe7`
-	Default Command: `["irssi"]`

```dockerfile
# Thu, 27 Jul 2023 23:47:11 GMT
ADD file:0a5e1e86b375d60637d0829f77a12085777cf2ca07495b0f6249d8efea84e958 in / 
# Thu, 27 Jul 2023 23:47:13 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 02:56:34 GMT
ENV HOME=/home/user
# Fri, 28 Jul 2023 02:56:34 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME"
# Fri, 28 Jul 2023 02:56:34 GMT
ENV LANG=C.UTF-8
# Fri, 28 Jul 2023 02:56:34 GMT
ENV IRSSI_VERSION=1.4.4
# Fri, 28 Jul 2023 02:57:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version
# Fri, 28 Jul 2023 02:57:05 GMT
WORKDIR /home/user
# Fri, 28 Jul 2023 02:57:05 GMT
USER user
# Fri, 28 Jul 2023 02:57:05 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4301d25bb1bea85fcc5b364aec84ff58274f714cea191ab22d9b1b1e4f78527`  
		Last Modified: Thu, 27 Jul 2023 23:52:17 GMT  
		Size: 27.5 MB (27489697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d504da7b1a5f43312d85ec53d90fcf308d4c926a327d4e9e08ae2c6cde66808`  
		Last Modified: Fri, 28 Jul 2023 02:57:35 GMT  
		Size: 18.2 MB (18206018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa851e13d6130f36fc6b7fb21ffce9a2e6f1fb944b19ce7d1fbe5e00c015e80e`  
		Last Modified: Fri, 28 Jul 2023 02:57:31 GMT  
		Size: 3.4 KB (3371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1290841f7c464f7b52e7b863a3d412f22f5b6d8f06ff45022160189446b84b8e`  
		Last Modified: Fri, 28 Jul 2023 02:57:35 GMT  
		Size: 27.2 MB (27227892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
