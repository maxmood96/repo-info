<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gcc`

-	[`gcc:12`](#gcc12)
-	[`gcc:12-bookworm`](#gcc12-bookworm)
-	[`gcc:12.4`](#gcc124)
-	[`gcc:12.4-bookworm`](#gcc124-bookworm)
-	[`gcc:12.4.0`](#gcc1240)
-	[`gcc:12.4.0-bookworm`](#gcc1240-bookworm)
-	[`gcc:13`](#gcc13)
-	[`gcc:13-bookworm`](#gcc13-bookworm)
-	[`gcc:13.3`](#gcc133)
-	[`gcc:13.3-bookworm`](#gcc133-bookworm)
-	[`gcc:13.3.0`](#gcc1330)
-	[`gcc:13.3.0-bookworm`](#gcc1330-bookworm)
-	[`gcc:14`](#gcc14)
-	[`gcc:14-bookworm`](#gcc14-bookworm)
-	[`gcc:14.2`](#gcc142)
-	[`gcc:14.2-bookworm`](#gcc142-bookworm)
-	[`gcc:14.2.0`](#gcc1420)
-	[`gcc:14.2.0-bookworm`](#gcc1420-bookworm)
-	[`gcc:bookworm`](#gccbookworm)
-	[`gcc:latest`](#gcclatest)

## `gcc:12`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:12-bookworm`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:12.4`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12.4` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:12.4-bookworm`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12.4-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:12.4.0`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12.4.0` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:12.4.0-bookworm`

```console
$ docker pull gcc@sha256:29b2aa718e1c95910666f9972a84c23b7b4c8150f836ae1557db87384d944187
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:12.4.0-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:ab84c890cea578b98a2cc7adcd4dc41a6e6fb9a287f6de7a3b8f47c926f0d78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.0 MB (490007621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be32b1d8eb3ba12b22a27bd6592851a6bd21dac3ae23259a22543049dba76f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340dd7281536b41cfe3c78c717ab62e2b7cc1e320b9c582271733df50c1aede0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 2.8 MB (2813332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a17afb825b0914fb6cf9633ebe6663653b883268e4a15330a6c878c24be8c7`  
		Last Modified: Tue, 25 Feb 2025 06:44:19 GMT  
		Size: 138.9 MB (138915432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8eb615bd5fd0cd8e0e979ce5b8e03adec0a830f38d4465f115309c4feba640`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 9.6 KB (9579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66936858fb2314bb2a1ae3ee99f74285e7d2f4558b1ff7a1a65d9ddf45c13cf0`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5dbc47bac9348cb691b1d12c86b5ae150ae2d77e44495e08e67600c229214c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034ec5b45a4150a479d302948677a17d2a31e2e454c8f8deeac4ce289527bdac`

```dockerfile
```

-	Layers:
	-	`sha256:42112bd85fd107cabaa473be33c2c62d1c096fb97c884ab48458c327ffd9b8f9`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8332b87b6477037b005c855918d52e7f820bfb2c329785f97da0b2aef745e1a`  
		Last Modified: Tue, 25 Feb 2025 06:44:17 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:3f4a071befa930a2263c4bdfbc69517d938d1b85b5c8b80de493ea44db7809a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429860508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ae437c206c94aa7ec2d4a41fd04a0cd215487f6e4aa12648307c59dbd59e83`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736019a4d81f08ba27129c4f174e81dae67ca35b18b81bd74658b12deec0ee43`  
		Last Modified: Tue, 25 Feb 2025 14:28:01 GMT  
		Size: 111.8 MB (111766700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360f69ee14b5e86ae6f7dce2894859f4cf1122c2c2080ab18b885e37d3e8030`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28cb8467843a7c16fc6adc9a74e5c233e5056764576ca3e46b565f576aa14d`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:854a0d5facfb36ca9dbd5378040d9d2807cd70ebe56f7d555d7699013768ae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf991cadfb35ebd5b439ba68c0e7855500231429d4df1e298b55e68e4964967`

```dockerfile
```

-	Layers:
	-	`sha256:8b299127b6971fc54cc9bcd5a18fa578a20c577cf281afbe225331bd7a69b050`  
		Last Modified: Tue, 25 Feb 2025 14:27:58 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7721479899e76dcbacbffd3b3920180e7ec3939a5c438f88de7555755465c3f4`  
		Last Modified: Tue, 25 Feb 2025 14:27:57 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:bf8e28df56313407c6d5029b50a44c8122ab0a313766cd68abc413940b3660dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.3 MB (407324925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ffaf328cd26c87e9651889c2740e165b2bc0dedbbbf0b895df453f30f0fe1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436908b91f9165028e6f64c377a1e1ca777d17964a8f16d0843a9f3d7fa004e`  
		Last Modified: Tue, 25 Feb 2025 21:05:33 GMT  
		Size: 103.7 MB (103711217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623f0b6b391136799616f6cf834d9af40217f96cce98e6f12271da75723224f`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e4026b6ed79a9227585c9e6b73690da348d8182a6cabeec2001893d19e95a1`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5e2280bfb3dd45404d4c60f00052caf7be4419013ba63f9ff49efc1b9bef1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3e74ace9abae9a14ea45e526d2e205799e57ea1e93b478fb2f48d5854c96b8`

```dockerfile
```

-	Layers:
	-	`sha256:6498f0ae64c04dc856cd63e400765049a31ea0c3bf54cad333d0ded4b918c304`  
		Last Modified: Tue, 25 Feb 2025 21:05:30 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80ad14f74a836010624764960ec99191c531a12f9d009358f0dd4921a12c328`  
		Last Modified: Tue, 25 Feb 2025 21:05:29 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:0215e7950e772cf00a3bee41cd1e17c3f636c3f34b27032eb6150c94e1c2a0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.5 MB (467480878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a712ce292e0a6cd9ee64b6394f4436c526d8a355f90532c1cc1a2990c9bcf509`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103e79d3be2c604c0306c0a29db1c6f2553faee5de2fa5fd32515162ea285fe`  
		Last Modified: Tue, 25 Feb 2025 19:12:27 GMT  
		Size: 125.8 MB (125760313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436edf026e0538f3807411ad83956a46d2643d5ce6ceed045948e886535ffa1b`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49423ac99576a8683aa83f2b2ee3c902d3380de2249756d74153c9c84be6285`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f09c5736259ea87cb614fccd1f9745cc894448d38018cf7bf6ca76d440c2b1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6cc40a950ee450c5a2b783db2bfc6ba105c1b8ab4adb8c66bc306d856e2000`

```dockerfile
```

-	Layers:
	-	`sha256:136db837264bcad92106dcbf8153a3d6559e0a9652a38045c313788cecdd157e`  
		Last Modified: Tue, 25 Feb 2025 19:12:24 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3154a2b113966f7a45fccd7ab26dd982e614e101629b0cecdbf58dcf9f3927ba`  
		Last Modified: Tue, 25 Feb 2025 19:12:23 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:250564c26acd5aa02da0172e8a8c6343b2ca9cc145403e947246b706c67b3b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.8 MB (502789417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f04d8b0db1d818aca70d28eb08ce590d698319b262ff1b4dda0f2ce16140`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d5d5f0eac42c065d0c34d35cd8e4b812d3dbb0b7717400267859062f73ab6`  
		Last Modified: Tue, 25 Feb 2025 15:09:04 GMT  
		Size: 137.5 MB (137543168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f29c9b42282bc8e7afc61d06490f6bd1112cf37aed72057707cfcf1ae02fe2b`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 9.7 KB (9713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd7c7ce9029f7a6ae2975a7537e2fbcac4201a033eb679c23713c308392d3d`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 1.8 KB (1805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:66c0d4c36a5ef107f39d47a44c961f2ecbd94866c413085308c047a1cc4742c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbedf0561cdd87126853c5979193c0dd33304bf9cf553fc700a2dae36e0ced2f`

```dockerfile
```

-	Layers:
	-	`sha256:f7be87670234186c95377071f0d69d98f56fcdbe8988de27620d6bef424bc2b5`  
		Last Modified: Tue, 25 Feb 2025 15:09:00 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdf6f28a84a8a701ea8bf817d138cba41d3eba865737c41a8f665e294f05bf1`  
		Last Modified: Tue, 25 Feb 2025 15:08:59 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12.4.0-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:ecc15ce2058743c6946e02093fe4760500d54a71367b3af13aca7e94a8ffffb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438398123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34826f63e358cde1176edb3776e19a1c03885de058a3a5093ea44dfbfcb1f1a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=12.4.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed3e9201dc5fbf884605f021c0792b61e5e8f30b8c18eecc6385698001c829`  
		Last Modified: Tue, 25 Feb 2025 14:21:42 GMT  
		Size: 117.6 MB (117611220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c01357dd01884c1352970b0bee54b493295dc932eda345bd76a30134ac1f9`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fd8d89c8b293743cc7198441314a0feb28ff62bc85a973384170ed5a266429`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12.4.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:1c04d2358a462e654b378e71d454f791b7a7d67d66914315f619313511b8a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1578da4b34e61063a371a72a5607428aaf6832cb0d787414012111a30601fb`

```dockerfile
```

-	Layers:
	-	`sha256:4173533184f93c6a5007da34604f00a262acd68b28497e0930cc92f73a04bbd8`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44e58f6988a6fc95371acde80a437e55b65b4d159f5d35f055806cdd5045ddb1`  
		Last Modified: Tue, 25 Feb 2025 14:21:40 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13-bookworm`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13.3`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13.3` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13.3-bookworm`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13.3-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13.3.0`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13.3.0` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:13.3.0-bookworm`

```console
$ docker pull gcc@sha256:03337b9c0aaaafe60c0543f401fcbc8b47f8efbd1cd01322a7b0392754f74e77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:13.3.0-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:34b9dfc878001eeb2b34c25ac7d90d66f71ab736b04cccf5c04db3c6fda09ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.6 MB (496558555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a23efbcaf4d579c5d40a10f23209da7ee691c52535d1771abd0caa4e64629`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc2c83efac1ca531a6c9d5325eb5c77636765c7a61ff4ead379d3932ebd457`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 2.8 MB (2813326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e599e367e116e9ce85f0015f97ce8e035cde32148f442bac57f5d9a3571e7d`  
		Last Modified: Tue, 25 Feb 2025 06:50:51 GMT  
		Size: 145.5 MB (145466341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd19e03ba91b5889af3802ff216339a1400838cb094f7e39c4349bcf7cabdcd3`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cb76042f310e9f0b144b8f17d0ec43a06caf765c6d2acd8f59e1261d5d6da7`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:dcde297b95cef585159599ec40dea565b27a004ede239253cb0e9667f58d7a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15535488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f111f4fe375442837f1efb2f2d110b175bfb252cc937b8a6876ed3051d217b7`

```dockerfile
```

-	Layers:
	-	`sha256:835997c1e3c88b0c63c2ecfd8bdcb253cb396fc4beb2b674ee8deaab7787525e`  
		Last Modified: Tue, 25 Feb 2025 06:50:47 GMT  
		Size: 15.5 MB (15505733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3124a8ef006c0f084a113e4df4b2ba8e7691cec33dfb81db7aa894c6d6c9c912`  
		Last Modified: Tue, 25 Feb 2025 06:50:46 GMT  
		Size: 29.8 KB (29755 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:e4958d1874405066a4ab3c3a7ac5490cffbf3b2888158cd4c3f92923e90fcc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.0 MB (436992469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4157c8285c53852728549ea2464ee69b4b0b018f333fe5a0d8c9c7e2c7b158d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0c67d8e4c510b19a775239ce98e58d5401b9dbeff59260e70048f429a7b40`  
		Last Modified: Tue, 25 Feb 2025 13:36:09 GMT  
		Size: 118.9 MB (118898647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fbada089e145c6c5ec461a649aa2060679339a62f7950c8a3d430c2fa9a305`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b220df9eb3e2458635bd0afc752f9108a46415864c50acd9a30c305750fe2d`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:db98c9db571ae8dbb6e12042f20b0f4aef1af5ec8013cb27f9aa6ca96f97c1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15334564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3bfc3d09e5e04348b6d1dbfadbffe6a46329bbbc277d521119e9899abda981`

```dockerfile
```

-	Layers:
	-	`sha256:18bc415aa9c9b71950ddc029e179ad321d75db277b632f05e54f7515fd23bee4`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 15.3 MB (15304677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81f1074ecb3899e956787bb980071187c0d224a7a6aab93d7fbbca865842dc7`  
		Last Modified: Tue, 25 Feb 2025 13:36:06 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:379d8f353abe3bf490a413284d70011880adf17ae43b964daf1bd878f7707289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414164328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2442f6733d2068ece6a1d27750fb0ca40ba0e38e89028297eddc0828cf5d5712`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db15a375395f1be3ed8fb54b3fa9160623525840264b49b825f5e62755bbfad7`  
		Last Modified: Tue, 25 Feb 2025 20:18:05 GMT  
		Size: 110.6 MB (110550629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bb6cc39760ac94693193dafd45ef045abfefbf33abaf852b73cfae7349d40`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f2d350e4d5e3ddce42b97cc429ba0dbbd2ede9f3ebf03f8c64aeddc33b983e`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:cf6b5a7627080f0592aca338eff270f980bb75363d9aedcfc99fcea66a9d557f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd6fe45cd6784a7123e546e3ddd1485b5349eff9685a728ad134ad2ab2f4205`

```dockerfile
```

-	Layers:
	-	`sha256:15032544902aa9da2a0fb48f93efe3c94121c87be36839377a32a9b88a57412a`  
		Last Modified: Tue, 25 Feb 2025 20:18:03 GMT  
		Size: 15.3 MB (15310155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1e5d86741969964c4b4d326ff789ded154747f82910e27c05f617b0be63621`  
		Last Modified: Tue, 25 Feb 2025 20:18:02 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:291d2fb4e0c3d3bd3b25bced0a30ce8cbe0ff638dcb1d2e2aa61ef9a4f069d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **478.5 MB (478546198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6587dd8c68580b457632c9341f3ce6dc01e2ca49233abd85de310e6167788fcb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8245a6cc0eee9b3a8e9bcbc93876ef15e76ef57f2ed98a4fcd34daaef73dc25b`  
		Last Modified: Tue, 25 Feb 2025 18:31:34 GMT  
		Size: 136.8 MB (136825642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11984f41b0134927eb0d58c8f2b4664204c6921582f0a49447f5507e4fd6989`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 9.6 KB (9595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c43c3ecd10e1f6913bb47c17a257513e9163e15bf798ea6144d37f46e1fa4`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:3081a22ff8951a047abbc28e4b9cb260d21a1a156f62f8c53aa672890967e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15564213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917d35cf906870b3b9b267531d98bfec0a55f1ddbfdf1a2097b8e8c5321f8065`

```dockerfile
```

-	Layers:
	-	`sha256:c5c1611bf4b1d1dc3b86fff32bf7e01fe0c6a0810f59f87d15379b3b416421df`  
		Last Modified: Tue, 25 Feb 2025 18:31:31 GMT  
		Size: 15.5 MB (15534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f1d6cca0f07616af8276d461f05b29f62e4c8937bfdf1b4ac6a53f1ba5c5131`  
		Last Modified: Tue, 25 Feb 2025 18:31:30 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:dd28cbabc9a7b957d958fc81246b4115d0793c2147024991bc5a5828b6565253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.8 MB (510780089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd54e8962be175e7ec5b11e65e1d852e4519ab265399a357893ae6703db57504`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3df0e3dbd477c15962157bc57be3075f1653cd1e038cc068a47cbd13b279ef`  
		Last Modified: Tue, 25 Feb 2025 14:24:47 GMT  
		Size: 145.5 MB (145533839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a45895bd88c8e785e8381c4571256772b05e7d7f4afe3b2e7d15c474b1caba`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3a02a9c77da90cd70d5670348ef95cca8e9c3349c881cbde74b70d10adda1f`  
		Last Modified: Tue, 25 Feb 2025 14:24:41 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:eaaafb18697183cb688d8b3ea7fc32938106f188c6b22cecc684851c78f7cab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15511962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b692b369a0adabfbc8934cf724890e9897dadd2a81c713066e546bee3739fc`

```dockerfile
```

-	Layers:
	-	`sha256:50c0af86f6f7a3e675d0563976bd0ac68c890dac7be7e38d4baa6b1b692bfc93`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 15.5 MB (15482144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b8d6867fbed68b19ee4496dc87cace2d9d1019d713c727dc1dcf29a9bd45172`  
		Last Modified: Tue, 25 Feb 2025 14:24:42 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13.3.0-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:22431e36aac201fbc1eb2fe248524fc93a09f894c00c9a4d1611e8374047aef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.6 MB (469558531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a5190e555505aef3726146928eacae913567f89f1cc48e3dbf864e8aa2ceb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 19 Jul 2024 18:36:25 GMT
ENV GCC_VERSION=13.3.0
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 19 Jul 2024 18:36:25 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f54fe0873ec696e16b3e827dfa0d3a056ae933ce6b9a7a59237782468de95f64`  
		Last Modified: Tue, 25 Feb 2025 01:37:09 GMT  
		Size: 47.1 MB (47129990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf373af35ad2775bc2760da2bd9da3eed720addbcb1c8757bc7daf70e4a1e57`  
		Last Modified: Tue, 25 Feb 2025 04:04:15 GMT  
		Size: 24.1 MB (24057741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb6f9e9e8249d179913a181aa58ad521b3c38990643e466d858925de6156c96`  
		Last Modified: Tue, 25 Feb 2025 07:16:48 GMT  
		Size: 63.5 MB (63498962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e021d44efecebbec440df3c3a0c980955996c77ad232ad735d9bc03286be04b3`  
		Last Modified: Tue, 25 Feb 2025 09:21:07 GMT  
		Size: 183.4 MB (183357133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d547d9c0dba920f9140c0a4f83e7d54db58ccc799816f598f6e12a4de8f33d2`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 2.7 MB (2731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d4afc625b63944502475546beaf2ee3a508e53a646ebda665a431af975aff1`  
		Last Modified: Tue, 25 Feb 2025 12:51:09 GMT  
		Size: 148.8 MB (148771626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a247d31c25a7e76590b9c75be922966f4ef7fe987684e61ef7ef3128c616f6`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 10.2 KB (10223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a91c7cba64881d957466c924def6e016cc2617774f50923967f349c104f95af`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13.3.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:310e03b4074b10ba69619d8d6c3d088ebbe7ba948d2078b56c2ead596a1a5d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15348179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f7c17fc8568de4f3729fd8b84c5735895e84bf96496b342899dffee02c99137`

```dockerfile
```

-	Layers:
	-	`sha256:92be973c1a6445b046039fe9babd351b3c90f5c90b970cc5ac743fb533b3cb19`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 15.3 MB (15318421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142ef19965dd7b5749025b5fea07f919c2ef7651425e78098f0cb12018ae6a53`  
		Last Modified: Tue, 25 Feb 2025 12:51:07 GMT  
		Size: 29.8 KB (29758 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14-bookworm`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14.2`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14.2` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14.2-bookworm`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14.2-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14.2.0`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14.2.0` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:14.2.0-bookworm`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:14.2.0-bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14.2.0-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14.2.0-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:bookworm`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:bookworm` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

## `gcc:latest`

```console
$ docker pull gcc@sha256:66e16b1fa454742ab2b310511e600bf732c436c76e6297ae0a94623938af95c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `gcc:latest` - linux; amd64

```console
$ docker pull gcc@sha256:1b0aa48d9987e7a7b56c9f64aad8318c2b211d071d49ac042e79761475f5b7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.8 MB (508825681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87992d0f205222132ff22f4b46f476598d7ec7ef8c3da4142cfedfb65a427b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8031108f3cda87bb32f090262d0109c8a0db99168050967becefad502e9a681b`  
		Last Modified: Tue, 25 Feb 2025 02:12:37 GMT  
		Size: 24.1 MB (24058530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d281e50d3e435595c266df06531a7e8c2ebb0c185622c8ab2eed8d760e6576b`  
		Last Modified: Tue, 25 Feb 2025 03:13:36 GMT  
		Size: 64.4 MB (64394215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447713e77b4fc3658cfba0c1e816b70ff6d9bf06563dc8cfcb0459406aed33b4`  
		Last Modified: Tue, 25 Feb 2025 04:17:49 GMT  
		Size: 211.3 MB (211338644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9057a850e9f73cae5e182aa315db53bdc15665084ebde7b61a3a127016cdef`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 2.8 MB (2813340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe1018c3be6e1bb417346205511033cdd727303b343469c4fce54374ce0253c`  
		Last Modified: Tue, 25 Feb 2025 07:02:24 GMT  
		Size: 157.7 MB (157733462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f565cd5914c8f318e8cfdd5790b803ae0cfd02af0b3db2f99b65b1ab16c64`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 9.6 KB (9600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c61c289655f74c2c19fe7bb87fcd59f6d8db62038027ecbf3d125baf17b5225`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:64b7a9fbe3d9169a2b6400d7b7d22abff62d9f14d022ef2e5d4c1426566891af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15536665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927079d8fcd991778cea603ae40344791f7084628fa8fefe974e45dc48b218ac`

```dockerfile
```

-	Layers:
	-	`sha256:aea9baf50cf5f1aef6af3fed40ad8f3385f288dbeb72f9b2ee73f38adb2d8a5d`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 15.5 MB (15506321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a220bd6506f1d4cab5c2310a6c3fa8e72e87bb90f8aaf0a314663517aee7f8e6`  
		Last Modified: Tue, 25 Feb 2025 07:02:22 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:latest` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b358b92677921efc0bdbefc7a93be0f079298611c09ced732e26ef77ef73cbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445553181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2454d7e906baf8412e6cc0ba53f4eb3519dac39bf45909be91b09bcb93f3fcf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e440391aafc3b52699d63063646c758a75255fbc01c9e7006a5c5d2a20c63f59`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 46.0 MB (46006498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c5ac7cafaf424134a147b31e5716a2caf29cf8e291b5c590ce4b2ebfd1938`  
		Last Modified: Tue, 25 Feb 2025 05:15:59 GMT  
		Size: 22.7 MB (22733290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918c63bcdb644d670948170f13621bfaa22910aa32373d99f809c5a6559fe442`  
		Last Modified: Tue, 25 Feb 2025 08:36:48 GMT  
		Size: 62.0 MB (62005949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cbd081ead96cf4434bcb703fbeb67e4eee91fcc6b7967eb51893e0eca7861f`  
		Last Modified: Tue, 25 Feb 2025 10:12:46 GMT  
		Size: 184.6 MB (184625882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79ee147b9aecfad2e0caa6c90d8be3fd7d620269ac5f3a1406d5c85e711e8c1`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 2.7 MB (2710918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641c90946e3f364165165bfddaac1e28c3af94ad0c759a235f2f911742dd2c7`  
		Last Modified: Tue, 25 Feb 2025 12:32:34 GMT  
		Size: 127.5 MB (127459371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e39ed04b510fac989ee03fe0bcd53867f4dde82661fb45f14d0f3d919127da`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 9.5 KB (9466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078f033aac98fd1b949a75770529ea51f65016ac5e77c996336fada867854757`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:77cddf6e734d69f5e7b8bd847ec583a662fb2b477b6309ba977a608dee78c577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15335772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf8f49fafd226f217f45b70f0e97ab0548b8bfba2cfc318e403c7972aeca28`

```dockerfile
```

-	Layers:
	-	`sha256:ba54b6bfcbf5a16a094d3efb8bab17867c148f8f41c409d250d21f8fc58f5b14`  
		Last Modified: Tue, 25 Feb 2025 12:32:31 GMT  
		Size: 15.3 MB (15305281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1683b93bf17d730a0c49f77e33534620bf05405f028a813ce460a54a5d7e7b`  
		Last Modified: Tue, 25 Feb 2025 12:32:30 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:latest` - linux; arm variant v7

```console
$ docker pull gcc@sha256:2a0a2bb8b49e0a6caca33dded042e25209bd74a5e0923ec0ed735a1c2375923a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422443169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2abcc9184c54b9237dc4074c03e33affcab18d311e299a4c273ff67ca0620668`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:453b261d63dad3de399026e1cfdba8f8449597be27e266bf531dc0b13b7b8e4d`  
		Last Modified: Tue, 25 Feb 2025 01:30:23 GMT  
		Size: 44.2 MB (44180294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c63e4627bc271627fc69fe799fe6c3e4205cb91260884ec880cb3ce5eb3d62f`  
		Last Modified: Tue, 25 Feb 2025 07:16:41 GMT  
		Size: 22.0 MB (21959970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394f90803fcb32c73d04e641359ad178fb7afcbc237af0f473479045797d2a00`  
		Last Modified: Tue, 25 Feb 2025 14:17:57 GMT  
		Size: 59.6 MB (59639886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4113b9663ae73fb9651693184bdc54017af95410f7a30b2a8c0f1f359581f15`  
		Last Modified: Tue, 25 Feb 2025 16:52:06 GMT  
		Size: 175.3 MB (175273090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32913c4205a2e1534d843f04aa77de225a59b3f7bcbc1e1bef8d25454095250c`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 2.5 MB (2549186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f2f9007514578a0d2e2f4c665954c1542a0f810e8c7a9a352c2507f2ee082`  
		Last Modified: Tue, 25 Feb 2025 19:24:36 GMT  
		Size: 118.8 MB (118829468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1486df19431d612ccf39cf8cf2c7801756ab54bc8bf088c603bae4fc63e8777`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb206f5c2e0298762bee3217d34a5553afdcfbaedb55cbda628e709330d20cd`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:bc4cda865704e2a4fc06515616594447de960bfa02937edb685877d42909eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e4f52645788a609d445007cdc7ebacb1c21c51de5b9ae362d04ab6479046c2`

```dockerfile
```

-	Layers:
	-	`sha256:908c9baee0e75d5c43d37be9e1f4c09c0008dfdb6633a8c02718f0b957106f87`  
		Last Modified: Tue, 25 Feb 2025 19:24:33 GMT  
		Size: 15.3 MB (15310759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b474f463ec00abeccff41a8cdae7b25ce15b563f0a88a7e9583d4c3bcc1d78f1`  
		Last Modified: Tue, 25 Feb 2025 19:24:32 GMT  
		Size: 30.5 KB (30491 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:latest` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:de0157ae4b1546d9b6363e1b6e6827ab9022de2cfed226370f4915130a9aa1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.0 MB (490983754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a62a4b69734d187d62b27076b145c08eea8b5f526e8343eb4239b05a26a3959`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d2532b9f392bc3320850b9e168122d70e866e881d59f4ce37ec5b22e4089d`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 2.7 MB (2733992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04fd2d971021dd8b128ba8895b86f4341eff7ff9f13fe4a2edf0387c0e1c118`  
		Last Modified: Tue, 25 Feb 2025 17:44:36 GMT  
		Size: 149.3 MB (149263191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cdafce8d0e360540722daf669793a3d81ad3e5884f0b7eebd97b974ac4e2a6`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 9.6 KB (9605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ebc78a335d44f802a428cee6ad3488f1b4e75bcfb4db5ef4efd79fd4ddb0a8`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:04a97ec625de97bb5431024d5736f082224b0f881959ec398ed57f1d797063cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15565437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b392c24d17ff1a0c9591127dc3fc82267ba631f8d5f5beb9fcc70545ed7f4`

```dockerfile
```

-	Layers:
	-	`sha256:6b79cf1475e52af850ab4714e0b0ecb9c0b478560d22e39ec309bb65510d6f84`  
		Last Modified: Tue, 25 Feb 2025 17:44:33 GMT  
		Size: 15.5 MB (15534896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d4db1eb3242cf35c01e5e782d5ab767e25056e7e6465217f21cb3ce0847e210`  
		Last Modified: Tue, 25 Feb 2025 17:44:32 GMT  
		Size: 30.5 KB (30541 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:latest` - linux; ppc64le

```console
$ docker pull gcc@sha256:622094fdcf4aa3cb7b2b0399c3ebd3c21597311dc07f90773957c79d62f73040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.6 MB (520589505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4211dcbd9b7d2c8e3332394f64cfa311cfea6bec94cd499c4a2dd3a80f5266`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:41ec7700671d083567ccdbece913b6f813c516be7736741723896d8ac522d7ee`  
		Last Modified: Tue, 25 Feb 2025 01:30:24 GMT  
		Size: 52.3 MB (52307654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c02c3136960f2879a5b4ad7a222a9530a6f17aa6969c50887d9421846cb46c7`  
		Last Modified: Tue, 25 Feb 2025 04:32:34 GMT  
		Size: 25.7 MB (25718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0251b4dd83d41da3c76cac0de0a694103ebc74f0c0a995ceaf43088bbca88`  
		Last Modified: Tue, 25 Feb 2025 08:19:25 GMT  
		Size: 69.8 MB (69843276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234b46aee36a62302335cbe22f7e0091ee4c09725e8b763895f9d5bdf5111acf`  
		Last Modified: Tue, 25 Feb 2025 11:49:07 GMT  
		Size: 214.4 MB (214371804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4bec5f7babaa0cc2fff836b9c04313278430ba48ce0e7aff415c3e1cb5752`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 3.0 MB (2993926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc3e102238dbc65c9d3d2428fd01c17f60d1877e86ddc164cf9a6d82d219857`  
		Last Modified: Tue, 25 Feb 2025 13:34:43 GMT  
		Size: 155.3 MB (155343243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb294b1607c1465bffcdaf01d0625072eaeecd1097c6f0f2af2be1a598830a`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 9.7 KB (9728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0065922e7e30686ba6599eb33e36067ba8531def099e1c76e09eabaefa8343ac`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:60957c26dd46bb8459e38a539270511a99377b380b0083bc4ae51f7526a4421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15513162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac9295e273cbd31879eed7273b30dcc81363faad538eafacfcbf0e5fefc9ad`

```dockerfile
```

-	Layers:
	-	`sha256:7100fcbb454e68e12fc12034ece8c985af802ef20f29a0edee2a6d5c6734f24e`  
		Last Modified: Tue, 25 Feb 2025 13:34:40 GMT  
		Size: 15.5 MB (15482744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a7b069921f5f5a10b8f09f29ab314bcaf9394e03716b1995589d74428b38`  
		Last Modified: Tue, 25 Feb 2025 13:34:39 GMT  
		Size: 30.4 KB (30418 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:latest` - linux; s390x

```console
$ docker pull gcc@sha256:aa71acd284efb91a615b7247aa290bf9df5a7df9f4818bbbf90453fb349410b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.4 MB (480445519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad13790815e1fcfa24ea1d3266ba66f6876828fd4dd2bc1a19b57420b488d9ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 01 Aug 2024 14:25:18 GMT
ENV GCC_VERSION=14.2.0
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 01 Aug 2024 14:25:18 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c45ea1e6cd72174d06b38f60dc6dc52a6c2774b6735a1659325d4ca9c9aa67`  
		Last Modified: Wed, 05 Feb 2025 02:15:01 GMT  
		Size: 2.7 MB (2731030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158b9ef85412138f432c2ee04bd56bd44df9e72800413f1669175210cacb4bf`  
		Last Modified: Wed, 05 Feb 2025 11:47:37 GMT  
		Size: 159.6 MB (159648858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6afbae25018b3cb3bd03104ec03e62564429a8d64a0256e5e70dca07b96653`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 10.0 KB (9965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fdf36bcc15120a15638c3c039d5e05c97b8e7b43be83de64fdd9bb8de3fb04`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:latest` - unknown; unknown

```console
$ docker pull gcc@sha256:420ef650ee0dbb4b7d21615e4c7b07a23459267aca0b1f2aa86f6362384739fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15349335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a9de9ada7dc53169a16ebe539c82640ab8abd79b8582b1e2f8a95641c0aa8`

```dockerfile
```

-	Layers:
	-	`sha256:f7802cd8cb78c9163437a656a35500f3c641ad1ed9ba61b4e147825561bb8347`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 15.3 MB (15318991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28966ff6448017d8b91b1a7fc03a0999545de2e6a639a1585b93b0fec694bc07`  
		Last Modified: Wed, 05 Feb 2025 11:47:34 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json
