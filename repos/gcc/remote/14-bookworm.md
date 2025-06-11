## `gcc:14-bookworm`

```console
$ docker pull gcc@sha256:9956b96810334f58453e17fbc7671f6943737fb05a9303e3db09061d1cff83c1
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
$ docker pull gcc@sha256:77bc0bf0cd62931e62002da8cde1ce956d8d076710fa742486c50445fb620aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.9 MB (508941160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7195d534bf73a640a26d1a396f4c14e447a574d99ae6fc0e1e73849ff6401d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167a126c1cc4c551c73adbd1dafe35fd269674030f1786a242fb4c51079c158c`  
		Last Modified: Wed, 11 Jun 2025 04:10:12 GMT  
		Size: 2.8 MB (2813357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c139aaf2d027616892ea313427ba5a9959ccf2bedde9ffa5306abca765c578`  
		Last Modified: Wed, 11 Jun 2025 06:28:14 GMT  
		Size: 157.8 MB (157836308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee5692bf6c855f433ae8a3a65a698bead64acf19811517d2d7bd7c8a69e7e2b`  
		Last Modified: Wed, 11 Jun 2025 04:10:12 GMT  
		Size: 9.6 KB (9613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837f99b4b804763a70f4bd3b17219faf29369ecd3c3b6485614989e735e7041e`  
		Last Modified: Wed, 11 Jun 2025 04:10:12 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60b28a8996a872ec61956abaf71d52ad51d08288bc5516d5b8d991a6a8883c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15925382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4986e98876559ba9071e33218cd1dfadf46c666672fd2d106c1b87c70d3b2ccc`

```dockerfile
```

-	Layers:
	-	`sha256:96364aa0a1c0c9f69be97bc51efdf59dc0d1a11c3ba25f968cac4211da2fcb0a`  
		Last Modified: Wed, 11 Jun 2025 06:18:58 GMT  
		Size: 15.9 MB (15895626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c8ccb8d853d6ee4b124a49384256781567908c33ec9e8fa9df487b16ef9d3a`  
		Last Modified: Wed, 11 Jun 2025 06:18:58 GMT  
		Size: 29.8 KB (29756 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:fa5f82adfdb906370662031b419a2982d4da1b91122211e4bd5bbb6af0f00021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.7 MB (445657400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283a1f648b664be1ba5a5241bf52ebcf850232a4bb6cdfb467766022c29d08bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2b51cc5977be0e2fae0a0314b991e4f90fafc6823a929775d09884dc18bcd7`  
		Last Modified: Tue, 03 Jun 2025 14:43:54 GMT  
		Size: 22.7 MB (22694185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662df94d663c1ee85e74f3b73f3f19049f9727ed40e72aa3497df0e6f9da2a46`  
		Last Modified: Tue, 03 Jun 2025 14:43:59 GMT  
		Size: 62.0 MB (61998014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567f3e20a3cd49e5c90cc3030da69c78ab60ff177b208c180331479f5965090`  
		Last Modified: Tue, 03 Jun 2025 14:44:03 GMT  
		Size: 184.6 MB (184635154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba952010ff68e6a3347d2352faeaf648bf6a92574757a065ad0f038d556f561b`  
		Last Modified: Tue, 03 Jun 2025 14:43:51 GMT  
		Size: 2.7 MB (2710956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdaea100d254b25fa6225c6ed0d7098a63839ad62e191a6c3d721050eadf8ab`  
		Last Modified: Fri, 23 May 2025 20:48:15 GMT  
		Size: 127.6 MB (127586341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b537eae3872030b7fcfba48f8d9bca5e0d99f9cf0dacd5fd513b0a3f157600`  
		Last Modified: Fri, 23 May 2025 20:48:12 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f067aad632f4342ab09833244b7e5a7efc8ef41e6d4e9708667367672f794fe3`  
		Last Modified: Fri, 23 May 2025 20:48:12 GMT  
		Size: 1.8 KB (1798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:a076cce00dc2f75e2b6e7bca09fb7243771646674c53f215098ca6ea50e20b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15429658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be057c74a6812b3c201af7810607ce475d6ba58414d2e304c747b2db844bb173`

```dockerfile
```

-	Layers:
	-	`sha256:d9aebafeee93569da803b082fadd3407f1ebf3f85a917d445d91136c73d01493`  
		Last Modified: Wed, 11 Jun 2025 06:19:11 GMT  
		Size: 15.4 MB (15399771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b1a7ded46ce1e874fb2804f6191ded4398c1447c3c58081d390b26452911d41`  
		Last Modified: Wed, 11 Jun 2025 06:19:13 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:6ca9316dd68fad0567be77b906569bce8aac03daa08ceee9bb8ddb71ac970885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422646961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4ffe8572810f92127b39c24c3da47cca5b39713f014a3ccb4683cd01aa33c6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106102cd8cd227bdb2ee9d96ae145ed0d301d3fdb4d0ca490ecd43926ed9b94a`  
		Last Modified: Tue, 03 Jun 2025 20:21:53 GMT  
		Size: 2.5 MB (2549296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a195753ab9f6370163c9045f37b8cf87739fdb8e3c7e1b5c6acbd50681256f27`  
		Last Modified: Fri, 23 May 2025 20:49:48 GMT  
		Size: 119.0 MB (119004897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4501dd87b8ec898c81e8662fded56730fedc5f623303119323db06c209711f6`  
		Last Modified: Sat, 07 Jun 2025 06:57:46 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c163b5623f8405b38dff484c3ae15ace801a62d0e7347a6f3204823e63b1be5`  
		Last Modified: Sat, 07 Jun 2025 06:57:46 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:eebe54f80126aa61864c44090244c103f2c8c7ce46b07cfa6fefaa8b5ba78c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15435136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e560e075f21174812736b99bb27ddc844682118a28436124b8c461d80662527c`

```dockerfile
```

-	Layers:
	-	`sha256:a5cebbdc939e7c2053d2578529b421e4a780fa42d7252932e6aa16db3969d266`  
		Last Modified: Wed, 11 Jun 2025 06:19:25 GMT  
		Size: 15.4 MB (15405249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c735118ce523d3d685692bb778852682c665f489433e217bd6244ae17c46eb9`  
		Last Modified: Wed, 11 Jun 2025 06:19:26 GMT  
		Size: 29.9 KB (29887 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:5452d6de4c7ea61328f081ad1cf721b89fca2fe9f84ab2be82d67a189acf3474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.1 MB (491125934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669cad8a8a82f34315f32c09c1d4dcb0358240ecac7abb29a4dc9456ef07c22b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaac9860927a6b9cca28b29893ee85e082d5e9c45131f7bc6360037e28e2443`  
		Last Modified: Tue, 03 Jun 2025 14:11:23 GMT  
		Size: 2.7 MB (2734083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00965a51478dab40065e10fe4bd7c57cc533cae001d55e9bb8bd6a5c3194f70`  
		Last Modified: Tue, 03 Jun 2025 16:14:48 GMT  
		Size: 149.4 MB (149377311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81154573bb0a2548634ae2ebf84c808db5071a55d07e09ecc3ffadec7b3ee5c3`  
		Last Modified: Tue, 03 Jun 2025 16:14:38 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a763ede0faa1f3e3182ce76fd04c0e898ee7a73fe326f79412f2b2e19e0ed2`  
		Last Modified: Tue, 03 Jun 2025 16:14:38 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:3e2bdf26974ac01118f95eb2485dace2b0a7dc35ccf5f750ea50eaad6a091e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15661234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245e637d157bc0be4816b1e867457475d87de143e637aff25fb3f530a5a08b6b`

```dockerfile
```

-	Layers:
	-	`sha256:8858302f978c8f186d30775738a27a51a79e61bfe7594af56573407d1be6af46`  
		Last Modified: Wed, 11 Jun 2025 06:19:36 GMT  
		Size: 15.6 MB (15631305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfed429d83a51327c8042d95df16ce4820623abef89b10999f7e6e529626cce7`  
		Last Modified: Wed, 11 Jun 2025 06:19:37 GMT  
		Size: 29.9 KB (29929 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:c584a01d1fa98080dee92db329a224f1461fd5a04e5f36a1ac5dc40ffb06cd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.7 MB (520722821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be79c89cd15506b140e45ebb3e074eea3cfad24c1788236d296a84cea53c3818`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367c013b078179861499c95f8c96d237be69ae2c9c587a18c2e702c0974b2c7e`  
		Last Modified: Tue, 03 Jun 2025 15:30:05 GMT  
		Size: 3.0 MB (2994025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bea8233bae2c6f13c91b6ca8e6fac8e3f3d3ca903cc3957839d7a214769264`  
		Last Modified: Fri, 23 May 2025 20:01:59 GMT  
		Size: 155.5 MB (155472474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57af3e4e33641f0305922afaece713fd56ad8574d3a24786f0616e97616d95c3`  
		Last Modified: Fri, 23 May 2025 20:01:54 GMT  
		Size: 9.7 KB (9735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ed04bc2e990e70ac3f002915fe6fe0ca996c7ae3fbee9899fe8ed9586040cb`  
		Last Modified: Fri, 23 May 2025 20:01:54 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:081f3cbfefc4ca2cb1b8b515db46cd8ee2fea8bc2e4b874001fda568df2b480f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15609106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9295c7dd5565cac6674ad16c0cbab3d896193ba9fc799ef1d112e4ab8704b5`

```dockerfile
```

-	Layers:
	-	`sha256:1bb14936a7d888bba36a5323032b88c330ec83c0c5607efff895ff464cb1fd85`  
		Last Modified: Wed, 11 Jun 2025 06:19:48 GMT  
		Size: 15.6 MB (15579288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5d2cb68c131157ffac540ba1758b2bb93c6236fdef28077d35c199e944f301`  
		Last Modified: Wed, 11 Jun 2025 06:19:49 GMT  
		Size: 29.8 KB (29818 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:14-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:2e51d618973add4ad6fd75a3959011c2e0fc0286b76a945717700b1197ea844a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.5 MB (480534767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c1a318e24f9b6bdd857c18ea78f3730714b70e70bd2cd9a2d2d0f3e7a2eb56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 14:25:19 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 23 May 2025 14:25:19 GMT
ENV GCC_VERSION=14.3.0
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Fri, 23 May 2025 14:25:19 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754aabb7db1aec2d402cef547b6ebcd74c06fbdfb6aa6a42d29c3481762681dc`  
		Last Modified: Tue, 03 Jun 2025 15:35:17 GMT  
		Size: 2.7 MB (2730745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63690dfb74bc29dc26313fb5d6e1278ce4865d1f847f7b252a395248b5939b71`  
		Last Modified: Fri, 23 May 2025 20:55:35 GMT  
		Size: 159.7 MB (159729655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fec783fca6996dce62b52ee5be9f26b322cc1ff6b51d54286b33e90f4dab31b`  
		Last Modified: Wed, 11 Jun 2025 09:25:55 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16b44c5ded99f2f60c2ccd4799367ce510110a2ae6b71d4ed15dd699281661`  
		Last Modified: Wed, 11 Jun 2025 09:25:55 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:14-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:ecef101beac29180eb0bca7771a345f0b490827744067e2b8c8e12ec0e469d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15443000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf4667c17ffcde3b3bf29240be31f92e1525264a05dccf2142f37f7c07dd5a0`

```dockerfile
```

-	Layers:
	-	`sha256:fa5c99bca5590746b00015b4586942e47f40067f05293de79143c07430548ebd`  
		Last Modified: Wed, 11 Jun 2025 06:20:01 GMT  
		Size: 15.4 MB (15413243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70098295fadbdf2b037d1a4a0248af212879c589fcde167d243b8746331cdb44`  
		Last Modified: Wed, 11 Jun 2025 06:20:02 GMT  
		Size: 29.8 KB (29757 bytes)  
		MIME: application/vnd.in-toto+json
