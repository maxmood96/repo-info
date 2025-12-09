## `gcc:15-trixie`

```console
$ docker pull gcc@sha256:0ce0b38744ff10282b446265b4ded84252a62657abad9d1b2a0e7a1648ea2317
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

### `gcc:15-trixie` - linux; amd64

```console
$ docker pull gcc@sha256:3285027d906ead0da2ca8a9edd41516ba2e083c0656d098946ee3bd7b6ce8281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.4 MB (551398644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab21fb6bab500a7658bbe3aef14e5cc4f818f3abe9470395eefef1b054b6f6ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:46:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:21:22 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 02:21:22 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 02:21:22 GMT
ENV GCC_VERSION=15.2.0
# Tue, 09 Dec 2025 02:21:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 02:21:23 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 02:21:23 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd420cee8193b72cf70974a80e88896c8e58d925edd1cdc515b203ff7aa65550`  
		Last Modified: Tue, 09 Dec 2025 00:47:38 GMT  
		Size: 236.0 MB (235974801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac2cd3aba3b1a9224404b7f08aa032475d2d3755f36838d6cd59c15bef9b123`  
		Last Modified: Tue, 09 Dec 2025 02:22:40 GMT  
		Size: 4.6 MB (4590055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778124c9c6f5166ae53cf49812110bd93b3bbf8d1dea19a7588b48ccb17159eb`  
		Last Modified: Tue, 09 Dec 2025 02:22:49 GMT  
		Size: 168.1 MB (168139123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c8711455c1079c474f5d680fbfd66b7ee1e59f59ea833809bff8776bffb9c`  
		Last Modified: Tue, 09 Dec 2025 02:22:40 GMT  
		Size: 10.6 KB (10629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45b2a03f20a858159b83b003bb7505aa328213e5db7eede0bc06ae39bac8278`  
		Last Modified: Tue, 09 Dec 2025 02:22:40 GMT  
		Size: 2.0 KB (2006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:67e216cd15b6e808e358b342aab5edeba2973d66d474e1c6b18c51a6ecc5e4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17411343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d140e4cf55c0ed49bd9eeaa2f4f8f085361b424d125a34edbb8069816ed08a5`

```dockerfile
```

-	Layers:
	-	`sha256:fa457630c94f54f43f014b904cd0a02e0be000d2f57e214772b29c5dc243bbca`  
		Last Modified: Tue, 09 Dec 2025 04:19:47 GMT  
		Size: 17.4 MB (17381059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a06c0ca2c0ea52c76d0b043af181bb1579cfe01c166b30d6bf1d392dc1d458`  
		Last Modified: Tue, 09 Dec 2025 04:19:48 GMT  
		Size: 30.3 KB (30284 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:15-trixie` - linux; arm variant v5

```console
$ docker pull gcc@sha256:7d6eae61cdbf19bfe0904362e0d509de5c897ecd704eb9e756afc0e642623543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **481.2 MB (481196808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f348daafccb6b4e2cf959733e83c8f35a3a98e5dff62761a96398951956990`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:15:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 04:24:43 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 04:24:43 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 04:24:43 GMT
ENV GCC_VERSION=15.2.0
# Tue, 09 Dec 2025 04:24:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 04:24:44 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 04:24:44 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaeb213e9fa41da55c6b895ce8273281464b3351c9fcf26aed8d0fc7484a18`  
		Last Modified: Mon, 08 Dec 2025 23:55:26 GMT  
		Size: 24.3 MB (24345927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4936999457f9b45cd7af5bc334afc3525d9cd25bc796f9420e78292f7e4e6d8`  
		Last Modified: Tue, 09 Dec 2025 01:18:47 GMT  
		Size: 65.3 MB (65318096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbe24d4bd7124e2e25624c6cb817a4ea96874b5b05fa82ee85e637d69cc11d3`  
		Last Modified: Tue, 09 Dec 2025 02:16:29 GMT  
		Size: 205.7 MB (205708128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe371d9f059264e2f791f79d335f4a2a3fd5a57eb745429c3abdf05bdc0c7d7`  
		Last Modified: Tue, 09 Dec 2025 04:25:29 GMT  
		Size: 4.4 MB (4439805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c9f8882733ad3edc2c45ffea8f02a5d884201d85d8a467e77d0245d1123a52`  
		Last Modified: Tue, 09 Dec 2025 04:29:47 GMT  
		Size: 133.9 MB (133924144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86a5b4bcbe63530acea1193a79aafb9d43e433e56dfee2a4a8e290a8c5c9659`  
		Last Modified: Tue, 09 Dec 2025 04:25:28 GMT  
		Size: 10.0 KB (9992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d52e7aa00622c7319e3c4372caa4915f91bad5129a9b1c809c8ae060d3fd401`  
		Last Modified: Tue, 09 Dec 2025 04:25:28 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:1ce2bb28cfe2b481f4fd67d13395097102e2d2d227c5a2361faf8dab60a9b5d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17173734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded464d44523b0a924447c271ceb68d2faef778ad7e5bf2ba8e4f0f4f519e8a4`

```dockerfile
```

-	Layers:
	-	`sha256:fa46b25abf128220b0507b0a260623c07c73b9cd66d026298c8deb5776207c83`  
		Last Modified: Tue, 09 Dec 2025 07:20:03 GMT  
		Size: 17.1 MB (17143301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43336e827bbcf400383205d5215b58055aa029456ba64e8a70f70acb31413609`  
		Last Modified: Tue, 09 Dec 2025 07:20:04 GMT  
		Size: 30.4 KB (30433 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:15-trixie` - linux; arm variant v7

```console
$ docker pull gcc@sha256:3fde40127e815b122786ec210428d42ab523e262f797677c76a4c604326e93c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.1 MB (454145971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab485a33372aa915957adc688519053e720fcc1ffba5d1ba6dedddafb13d72d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:19:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:19:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 04:26:23 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 04:26:23 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 04:26:23 GMT
ENV GCC_VERSION=15.2.0
# Tue, 09 Dec 2025 04:26:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 04:26:23 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 04:26:23 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f0a24772dec0e72cc1a314a0c6613a5577b09b7b6c8368604b9a163a31aa5`  
		Last Modified: Tue, 09 Dec 2025 02:20:05 GMT  
		Size: 193.3 MB (193258585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90052f3397d351538642889619bc2798da7f77ad7f3e5bc637200e72bf1bac5a`  
		Last Modified: Tue, 09 Dec 2025 04:27:04 GMT  
		Size: 4.2 MB (4206548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872eede6d335cf8853c077812325508197666c35150e4309462fd97d6043c013`  
		Last Modified: Tue, 09 Dec 2025 04:27:10 GMT  
		Size: 124.6 MB (124616955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1984207825585a1f9db6fce08b777b86928b3ffa9fad1305a2ab8138614c36`  
		Last Modified: Tue, 09 Dec 2025 04:27:04 GMT  
		Size: 10.0 KB (10015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62880501de2446c3ca2c897e1b847da8c10a89810eaf7042effe62cf082578ef`  
		Last Modified: Tue, 09 Dec 2025 04:27:03 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:990556e85140edb16b51bd7ca99714db06ccf60c0c4c5f13980e27dc35f89f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17179534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81890d7d47689636d46c2ec88c1fb11f19fa46d8910279529a234b7582624309`

```dockerfile
```

-	Layers:
	-	`sha256:c65acdf35502f3a476585561a594a46f05cb82af45bcb4dd5f7cab859a2b1d5c`  
		Last Modified: Tue, 09 Dec 2025 07:20:17 GMT  
		Size: 17.1 MB (17149099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b80960141335a0ec4852f85f1784d0e2e9fa03884a0d0c9529f6df56c7e28fc`  
		Last Modified: Tue, 09 Dec 2025 07:20:18 GMT  
		Size: 30.4 KB (30435 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:15-trixie` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:d24c97059f66d4d08448d3242e0e88a3f14684def3f2677ba295cf0cb7ea800c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.9 MB (530870032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0017d7246c9f4e57e2f6b155c859b4a310c43afab8f5bc49e26fbdb73751d35`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:16:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 03:11:22 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 03:11:22 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 03:11:22 GMT
ENV GCC_VERSION=15.2.0
# Tue, 09 Dec 2025 03:11:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 03:11:23 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 03:11:23 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b4af09d0743acafc293109ad1b191f5a03a36cd1dddf8454458ced3631f5d`  
		Last Modified: Tue, 09 Dec 2025 01:17:36 GMT  
		Size: 226.1 MB (226108094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e91876258b81ed1167978489ddbffca1c7cf882f8eab2bb5efe8c63690790b0`  
		Last Modified: Tue, 09 Dec 2025 03:12:32 GMT  
		Size: 4.5 MB (4498257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3448aa96890c58c7938059854a7ffc7ad3f43aabd9450867aa104b15499b026`  
		Last Modified: Tue, 09 Dec 2025 03:12:46 GMT  
		Size: 158.0 MB (157995218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc845fb54ceb735ff814a62e8f0efd0c8f0075ef4f411109b799f46e05cbbe2`  
		Last Modified: Tue, 09 Dec 2025 03:12:37 GMT  
		Size: 10.3 KB (10286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1b3211ee38bc1d91493d7802224b8b1e46c21df3679f3b9a177b9a8cccd295`  
		Last Modified: Tue, 09 Dec 2025 03:12:32 GMT  
		Size: 2.0 KB (1996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:657d26b2b56f00e3f43b5a8ce7f00957c42298663e18d296b70cea78ac68d2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17495899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d686b24b07205c0ec5f2a25f5835997c34bd17eb65a67c5ec5f9f13b904e864d`

```dockerfile
```

-	Layers:
	-	`sha256:b892f3c8c458e1777c1f9f622c3d887de38416d7c60b693051e8223bf4effb1c`  
		Last Modified: Tue, 09 Dec 2025 04:20:24 GMT  
		Size: 17.5 MB (17465417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bfa746ce1a8b80f6031894d23607e679b103efc8ea1ebdc6464c503b3acd31c`  
		Last Modified: Tue, 09 Dec 2025 04:20:25 GMT  
		Size: 30.5 KB (30482 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:15-trixie` - linux; ppc64le

```console
$ docker pull gcc@sha256:65ab6f6eb38a72c470daa5dc0138ac05acd4be4c1a6fa030e69ab9be16679a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.5 MB (553522928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da728532f038373ee66db6a5f7d64327e0bd5e077098f1f0c238acc40cab0ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:22:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 09:19:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 10:42:18 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 18 Nov 2025 10:42:18 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 18 Nov 2025 10:42:18 GMT
ENV GCC_VERSION=15.2.0
# Tue, 18 Nov 2025 10:42:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 18 Nov 2025 10:42:19 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 18 Nov 2025 10:42:20 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c7b0e7e39934178ce53a9a8f734eb91b249eb1d93ae50bc043579a195efbe`  
		Last Modified: Tue, 18 Nov 2025 12:40:13 GMT  
		Size: 231.1 MB (231098714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc9a8168c60af8bdc5bfb4f89f938a3fb94d2a2a86865ae7c31dabd935f178a`  
		Last Modified: Tue, 18 Nov 2025 10:44:38 GMT  
		Size: 4.9 MB (4896676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01f5ef9c649f515c75ccf26ef1304f3d3c88612462964d041330270d467e5ff`  
		Last Modified: Tue, 18 Nov 2025 16:07:54 GMT  
		Size: 164.4 MB (164387533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f087c5ba420d99e270694482233c754869cbaac4e1f5e6330647fd679e5d9d4a`  
		Last Modified: Tue, 18 Nov 2025 10:44:37 GMT  
		Size: 10.7 KB (10691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ad326ba39c501665294b3611c59b7a92acee04f91cd55b790562f0dc5cda23`  
		Last Modified: Tue, 18 Nov 2025 10:44:37 GMT  
		Size: 2.0 KB (2007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:939e86b21c484d21fdc437420118bcee82a7497b262520e005cba98be2a2d952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17396997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ff92d7bb3f9e9b5af634faf448a5a8724474909fcece0b987ecc95f94da4b`

```dockerfile
```

-	Layers:
	-	`sha256:085c4df3938293bd32121bc0c0c4fe9d5ed5162afdc69d6425d4e44979645b4a`  
		Last Modified: Tue, 18 Nov 2025 13:19:43 GMT  
		Size: 17.4 MB (17366638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc64302f3a09b09a2cc36a0cfd17ba7470959fde0cdb7520a2860f5a49d3da5`  
		Last Modified: Tue, 18 Nov 2025 13:19:44 GMT  
		Size: 30.4 KB (30359 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:15-trixie` - linux; s390x

```console
$ docker pull gcc@sha256:034d70dec4d4b834cf88de29eef684b7a8a2565c33d45d595013e2faa059164a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 MB (522139041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688dc6826dff93e50903dd0937e3fea9d629d213970f25c70fa2f8d9dbf2b422`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 05:03:10 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 09 Dec 2025 05:03:10 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 09 Dec 2025 05:03:10 GMT
ENV GCC_VERSION=15.2.0
# Tue, 09 Dec 2025 05:03:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 09 Dec 2025 05:03:11 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 09 Dec 2025 05:03:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d6b6af65161fdf6adbca5b49fba0d0a414708fb199521ee78075952e4ba4ca`  
		Last Modified: Tue, 09 Dec 2025 02:59:04 GMT  
		Size: 206.5 MB (206478489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f41355e6c8a42aa0e1e4dab4c308ae3fb2631ce0f148f90833808849151aa96`  
		Last Modified: Tue, 09 Dec 2025 05:04:21 GMT  
		Size: 4.7 MB (4672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534cf45398237fc100534875afec952018f8f1a75e1ab4c917822db024a710e0`  
		Last Modified: Tue, 09 Dec 2025 05:04:38 GMT  
		Size: 166.2 MB (166218761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87a74122086c123fa79ba3209dd0cf305b0431c38c565e07953fb5c2925e1b3`  
		Last Modified: Tue, 09 Dec 2025 05:04:21 GMT  
		Size: 10.8 KB (10814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd388ce98997b2e85c7ae57cf1b13c68ce524f94e876ccff45cafa67e4ae8845`  
		Last Modified: Tue, 09 Dec 2025 05:04:21 GMT  
		Size: 2.0 KB (1987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:15-trixie` - unknown; unknown

```console
$ docker pull gcc@sha256:a7c02be58727e6ddb948623b35768ac29d096b48f3d2f62348f314b85b9cb8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17188573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2772e5086566a3612cc550238afa335491d3972073cb4e13a5258c616910980`

```dockerfile
```

-	Layers:
	-	`sha256:4ee87d2e27bfc879c6cafa10a19c71a2619d242cde2912624d84491e052299ed`  
		Last Modified: Tue, 09 Dec 2025 07:20:48 GMT  
		Size: 17.2 MB (17158288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5130741d39c3540870f16eb1aeca7c7fbecb4f4dd8f7030c88c6f9f06974f7`  
		Last Modified: Tue, 09 Dec 2025 07:20:49 GMT  
		Size: 30.3 KB (30285 bytes)  
		MIME: application/vnd.in-toto+json
