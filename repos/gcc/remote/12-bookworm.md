## `gcc:12-bookworm`

```console
$ docker pull gcc@sha256:fa6eab45dd797e7fe238cf40163cfc7d4b29613eccf015464fd9b4a74c66fa6b
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
$ docker pull gcc@sha256:b17e3562f470d3dc821d4a9780996cd255338d64390ba523a51b2b8cbffe6718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.3 MB (490294363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c25b5a9e0d4460782e71ed0ce72e3ff8d921fbec00de29bad94e45d3a674163`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:44:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:22:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:36:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:20:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:55:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 30 Dec 2025 03:55:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 30 Dec 2025 03:55:01 GMT
ENV GCC_VERSION=12.5.0
# Tue, 30 Dec 2025 03:55:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 03:55:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 30 Dec 2025 03:55:02 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16afb0fdc4694732853f4fbf5125c1dcb35f20cca5bec77a98d73d0d3124f855`  
		Last Modified: Mon, 29 Dec 2025 23:45:17 GMT  
		Size: 24.0 MB (24029344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858b7813255a9cb57d05f02b50978e5b5965b0cfc040288fa29905cdc65ad9a`  
		Last Modified: Tue, 30 Dec 2025 01:22:58 GMT  
		Size: 64.4 MB (64396090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318d61060ae74f5254974208e92a54f807b028710293f41900249bc6033acf41`  
		Last Modified: Tue, 30 Dec 2025 02:37:17 GMT  
		Size: 211.5 MB (211466563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f2e0b8207c03754e397bb352e16be131a5e5811fcf81ee15cd753c708b70d3`  
		Last Modified: Tue, 30 Dec 2025 03:55:40 GMT  
		Size: 2.8 MB (2813848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd37b3123202e7a95036fbec2a28832fc6ef735fac57a6e9c554f912c20f95ca`  
		Last Modified: Tue, 30 Dec 2025 03:56:02 GMT  
		Size: 139.1 MB (139096353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f373e27990fe1d2700440ca9929b764b298e063b74e7513e2b1be995183138b2`  
		Last Modified: Tue, 30 Dec 2025 03:55:44 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d799db4aa2d9ada241fca30de850094258d92e3bbfd50408fc7248ea9a0808`  
		Last Modified: Tue, 30 Dec 2025 03:55:40 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f2332807f31334a86b9c5a3d4f53e36408562886abb80f752376daa2332ba473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15933071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407070bffdb1380915e20b3ec76ee558a045ab9cf68caaddd02f75b7ffe3f059`

```dockerfile
```

-	Layers:
	-	`sha256:f664690a345f261be127166c562be5b05559ab5476f8d8819ca19fcef732b38f`  
		Last Modified: Tue, 30 Dec 2025 04:19:13 GMT  
		Size: 15.9 MB (15903358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73dc99f5a23bd355509daafd7fb48db7a21190e216a7e6d1847c88341512ac57`  
		Last Modified: Tue, 30 Dec 2025 04:19:13 GMT  
		Size: 29.7 KB (29713 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:0854fa15a0010c88d5b863f0200408d80d64ef8d5da37781655c9526933a1c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.9 MB (429943805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad89ec0872c25d5a50603d949cad32fe6cadd7784d6b890e753684d9847f6ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:13:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 03:19:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 04:07:03 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 04:07:03 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 04:07:03 GMT
ENV GCC_VERSION=12.5.0
# Tue, 09 Dec 2025 04:07:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 04:07:03 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 04:07:03 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f70892cf40cf00afad948163124cb46c26422ae7a58c48384378f9afd91c3e5`  
		Last Modified: Mon, 08 Dec 2025 23:53:57 GMT  
		Size: 22.7 MB (22705745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8089c2b20fedea36afc932499843f6245377677804c10ff2c0e867c4b27513c`  
		Last Modified: Tue, 09 Dec 2025 01:18:41 GMT  
		Size: 62.0 MB (62010644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf65146386f6d1636f8e6d20118575504aa19edbffdf36f5cafe418ddd2909b`  
		Last Modified: Tue, 09 Dec 2025 02:14:32 GMT  
		Size: 184.7 MB (184720504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ce73ef1c645bad12bad57753041b6c79de1c27263880b55f0f77d438b08193`  
		Last Modified: Tue, 09 Dec 2025 04:07:43 GMT  
		Size: 2.7 MB (2710949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ca9152837a417f5d4772c2683035d09e2937e51343b6f4da013182490fe4e`  
		Last Modified: Tue, 09 Dec 2025 04:07:52 GMT  
		Size: 111.8 MB (111769096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892297631d6a1997296c5d3a314e1bf91433e21484c6b2f6c720ca9348ca90d4`  
		Last Modified: Tue, 09 Dec 2025 04:07:43 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eca16f34066b536a1de57c211862f2d2c835176d7437313851dd1ad6f94ef7`  
		Last Modified: Tue, 09 Dec 2025 04:07:43 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:000917e3d98540d0608c3e6628d5e7f45e5462137a9325e9d8b87bdda4dcb386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15730170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d26973ec661287e00c0c865f3436f3e32f8348f3f5a81a55b9e88739a71fab1`

```dockerfile
```

-	Layers:
	-	`sha256:bc6633bbcedd36d20f308e77c3e873f8bfd158ee1c439712640a2c57351bf83b`  
		Last Modified: Tue, 09 Dec 2025 04:18:50 GMT  
		Size: 15.7 MB (15700322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3895167cfa4e5c35652ca793967e4ee5babe9d5d3258ed1f317f19db1e11d808`  
		Last Modified: Tue, 09 Dec 2025 04:18:51 GMT  
		Size: 29.8 KB (29848 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:28f65bb496ba161aa2d53b2f59159d1c6cf805d2992223581dae260012eb7432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.4 MB (407424416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145f97ab1e143abdf0363730e63b4de32a94ece47172f38a374115bc112c9cba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:17:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:03:59 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 30 Dec 2025 04:03:59 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 30 Dec 2025 04:03:59 GMT
ENV GCC_VERSION=12.5.0
# Tue, 30 Dec 2025 04:03:59 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 04:03:59 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 30 Dec 2025 04:03:59 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e89c6396ded32c2f8dc71a0c5aae48558ec631543500fcbbe7dbc428401a7361`  
		Last Modified: Mon, 29 Dec 2025 22:25:09 GMT  
		Size: 44.2 MB (44196130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb8db5ae0eab82c780cd4fa20967bd3633799cf8ed89cd7858d72dcce53203`  
		Last Modified: Tue, 30 Dec 2025 00:33:50 GMT  
		Size: 21.9 MB (21934762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7f06489595662b32227ed4939431e5099ae83a2661a5770c752a389e68e400`  
		Last Modified: Tue, 30 Dec 2025 02:06:44 GMT  
		Size: 59.7 MB (59652384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3429e4481c959b42472aeab211da596c017178158219b524e556cb5c3ee4987`  
		Last Modified: Tue, 30 Dec 2025 02:35:40 GMT  
		Size: 175.4 MB (175370783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf6117aea4985ec4c656007273210381ba8134076d75f86c3fe4803727fd049`  
		Last Modified: Tue, 30 Dec 2025 04:04:36 GMT  
		Size: 2.5 MB (2549294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8cd0a444d84524243a39b5ef7c74dddbdded94a31fb13e66efa9f9b47e4809`  
		Last Modified: Tue, 30 Dec 2025 04:04:51 GMT  
		Size: 103.7 MB (103709991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18ef3dfb172a24908fe161b91827dbffc3f7c8e1e82397e35b8900d99945de0`  
		Last Modified: Tue, 30 Dec 2025 04:04:36 GMT  
		Size: 9.3 KB (9279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0d1d79bae23090333de292d84da1b5861dafb1d8e7337401a463227f08d054`  
		Last Modified: Tue, 30 Dec 2025 04:04:36 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:d403ba2a9040cf90147cab6b8d832e782b924be77b764ed5a7e4a77ae84aff8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15735704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517584c3cc2eed2e5b53dd584aec5d9bd69343a5ea67e95c0c38597214f50770`

```dockerfile
```

-	Layers:
	-	`sha256:8378a7053dff8640716b03b3a0586c1fc8005a3419a74c8a916d14f0f5cd3eee`  
		Last Modified: Tue, 30 Dec 2025 04:19:35 GMT  
		Size: 15.7 MB (15705856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4f8d94be527d33676d65d1210af7c82b8f005868fa3be844dde9b58ebc5c32`  
		Last Modified: Tue, 30 Dec 2025 04:19:36 GMT  
		Size: 29.8 KB (29848 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:126321d73bbe490fdda5eb181fd31b0bd2dad3bd7b7a522a5950175234d88d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.8 MB (467821982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59fcac5b1d739ad58df0fc92cf1ea34edf5d3f12aff7624174e2109254f62f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:35:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:20:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 03:58:49 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 30 Dec 2025 03:58:49 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 30 Dec 2025 03:58:49 GMT
ENV GCC_VERSION=12.5.0
# Tue, 30 Dec 2025 03:58:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 03:58:49 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 30 Dec 2025 03:58:49 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b14a03c2e7665cfd5dcf91d78e753eaacbe124548ced748ccf44fdc600c28e4`  
		Last Modified: Mon, 29 Dec 2025 23:45:53 GMT  
		Size: 23.6 MB (23598380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885a684c982cb8679ba82c9c939ec2b3cfe9c823a68d404ebbc3ac75d14830df`  
		Last Modified: Tue, 30 Dec 2025 01:25:21 GMT  
		Size: 64.4 MB (64371168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e473cfa5c6fa57db72a6e347d7fc4f13909c3c9e83819127a50c0195b88eae`  
		Last Modified: Tue, 30 Dec 2025 02:36:21 GMT  
		Size: 203.0 MB (202980659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3424fc1e45734818d42a2aabcf213a7ba33637ba7a66f02466769cb46c14b1`  
		Last Modified: Tue, 30 Dec 2025 03:59:32 GMT  
		Size: 2.7 MB (2734160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9e3e1563a08d326e909123035d349722dec9b37be2ffd706f32d5df7d96e7c`  
		Last Modified: Tue, 30 Dec 2025 03:59:43 GMT  
		Size: 125.8 MB (125767261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553c58e6120416008ac936a6dd4b27877e7b4d8cb72a36df46952a42faf70d23`  
		Last Modified: Tue, 30 Dec 2025 03:59:31 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c516148ccbc0ee7cc72105472e76f4a88e51cb15f8db133313abd13ee33a781`  
		Last Modified: Tue, 30 Dec 2025 03:59:31 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:fcb293f281cfe2224b1855ae08076fef10b158e250e6fab2095ac4efe006ad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15961796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ea213553abf2fb14d6d7823da90558350422b4652a98d5594a2ef4431e1507`

```dockerfile
```

-	Layers:
	-	`sha256:3726e6cfcbd0b2bcda6e80243ea698dd5d424d0a6f814e1d1f046711eebfd8c2`  
		Last Modified: Tue, 30 Dec 2025 04:19:47 GMT  
		Size: 15.9 MB (15931910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71fe929e2856a5caed16094468537939daaedf943eb9835b3dbc02ddf4f554d7`  
		Last Modified: Tue, 30 Dec 2025 04:19:48 GMT  
		Size: 29.9 KB (29886 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:57fe879fc3ff60c3ed92658a1e5389b732de3cc77234faf588bc75d175c6f0c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 MB (502903367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39b5e2856b7ec939e2b816fe0c94f077a522ec5d196b820bd1fbbe4b7d4180`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:09:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:13:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 06:18:38 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 06:18:38 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 06:18:38 GMT
ENV GCC_VERSION=12.5.0
# Tue, 09 Dec 2025 06:18:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 06:18:40 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 06:18:40 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc15b235f2d99c9b8cb7f5511247453daa35498d32335b3432bc90fb1d754bd`  
		Last Modified: Tue, 09 Dec 2025 02:11:48 GMT  
		Size: 214.5 MB (214498018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ae940952ef2f2079b46de8bbf631d8dba17e7d48e203d6fea43c6721db7cdd`  
		Last Modified: Tue, 09 Dec 2025 06:20:30 GMT  
		Size: 3.0 MB (2994255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8908997dde26590e4b53295937b25c80df4517c8d4ca589ea506e0210c98d69b`  
		Last Modified: Tue, 09 Dec 2025 06:20:48 GMT  
		Size: 137.6 MB (137554357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242f1d74005528e66939f7eb36cdce8b2c68733e4ee8245fa31304550e9c1655`  
		Last Modified: Tue, 09 Dec 2025 06:20:30 GMT  
		Size: 9.7 KB (9729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f68fa024d91a90365025d1ce8a80c2db703a339be3392f281a5f2645be7949`  
		Last Modified: Tue, 09 Dec 2025 06:20:30 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:1d5439adbf1d4c00bb1d86f822b0019837d88a37fee426809859591997a086d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15909626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8955191c770a53605c2cc2aacacea9a9743d690575c2fe423d2073914d47c19e`

```dockerfile
```

-	Layers:
	-	`sha256:737cc63a371d6b756d11f8507223cda9768f729868e0abff7eeb336dd3c521c3`  
		Last Modified: Tue, 09 Dec 2025 07:19:20 GMT  
		Size: 15.9 MB (15879851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f46a7ffb0b61fb4911905fcf4d67e6549f4b0eaff6b33781643637dce57db2`  
		Last Modified: Tue, 09 Dec 2025 07:19:21 GMT  
		Size: 29.8 KB (29775 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:38251a482b5bc0f4fc80e603d13b3d0cb06b32387fdaa012a965bf0576b88237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.5 MB (438513125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46386a75509767e8fd746a98c3e08364ddd5e8e706875b08a0777c0902c418`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:57:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:15:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 05:15:11 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 05:15:11 GMT
ENV GCC_VERSION=12.5.0
# Tue, 09 Dec 2025 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 05:15:11 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 05:15:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021709bd5f44ac18c83367b46ae0ee36d6bf3bfbaaee7f0fc2b3f5a37fa60847`  
		Last Modified: Tue, 09 Dec 2025 03:16:04 GMT  
		Size: 183.5 MB (183497520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4493c3f58524acd1e5d1c125e8e244a45d48ee89ef82019c1daf8ee2a82b5d`  
		Last Modified: Tue, 09 Dec 2025 05:16:08 GMT  
		Size: 2.7 MB (2730947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e426f0b1f8dbfece8efdfb7f63438921fb4483fbe1654ab3e8be0692d03750`  
		Last Modified: Tue, 09 Dec 2025 05:16:19 GMT  
		Size: 117.6 MB (117606596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae780a9af9d0fcaa9af42ec55f75b58b64429bc240ae6f8df0d77209df0d5f49`  
		Last Modified: Tue, 09 Dec 2025 05:16:08 GMT  
		Size: 10.1 KB (10092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daab87e1e213dc1fb2f053d7dcd0e046da0037f520b4af8c8b6dac85f81e803`  
		Last Modified: Tue, 09 Dec 2025 05:16:08 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:dd6887829340bf8fa12033c5fb1c4f9624abf67b8bc5f93fb75fec53e6d5e05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15740615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aedacd96aa78a9b9b45e4fa63fb6ffddc243938253812af9132dd66f65423d`

```dockerfile
```

-	Layers:
	-	`sha256:64a32536f5e3832da1cae473b7ebf847f6af3c26cf0179435fe8df6860a258a3`  
		Last Modified: Tue, 09 Dec 2025 07:19:33 GMT  
		Size: 15.7 MB (15710900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d136f6dc75faa0f3016734659b1ccc3e99e3f42cd68edc43dc4ced912b7e8f16`  
		Last Modified: Tue, 09 Dec 2025 07:19:34 GMT  
		Size: 29.7 KB (29715 bytes)  
		MIME: application/vnd.in-toto+json
