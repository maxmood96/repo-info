## `gcc:13-bookworm`

```console
$ docker pull gcc@sha256:f0e3a9a1d9dd8df290df776acee7d64ea2bb2b3abb470ec3701af9140ca1692b
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
$ docker pull gcc@sha256:644581bd1f563d821efe8078659cfd9ac80d6bc7b3e64296963a1ab9cf586128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.3 MB (497266442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e3af35ed3635e97eea5c5589235f1591b333a6cddf388e10489c711858576`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:43 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
# Thu, 13 Jun 2024 01:20:44 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:39:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:41:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_VERSION=13.3.0
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5651b5803b186603909f6c77cdff7bdd4ba7ab8ca4ebccb5a6b0be9037b4e5b6`  
		Last Modified: Thu, 13 Jun 2024 03:49:21 GMT  
		Size: 24.1 MB (24050013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3873416e6a335157d669c6193a256dfb289331d669d87f200e4eed1f19f9ebb9`  
		Last Modified: Thu, 13 Jun 2024 03:49:40 GMT  
		Size: 64.1 MB (64142031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a142b8b0e695954ed154c13c098ede4e217dcb99aa7158e34361604191822bd`  
		Last Modified: Thu, 13 Jun 2024 03:50:15 GMT  
		Size: 211.2 MB (211206915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484031d185ed94218ba91068a4e92b66ad6873745286343d0fddeda94c57bfd0`  
		Last Modified: Sat, 22 Jun 2024 02:36:41 GMT  
		Size: 2.8 MB (2813196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15a1bd58b18246183f951a3c5add19930cd6822b840212ad60dba6771f36458`  
		Last Modified: Sat, 22 Jun 2024 02:36:44 GMT  
		Size: 145.5 MB (145466203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436c069c0dc45206726133ff0de28e31d75593e7ec8710ce0e8255fd0fc9e47c`  
		Last Modified: Sat, 22 Jun 2024 02:36:41 GMT  
		Size: 9.6 KB (9647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ecfb6b060f6337d7a369c13cefc6187564c517a96609b58beec974a07ab443`  
		Last Modified: Sat, 22 Jun 2024 02:36:41 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:e3b878df762a74467029c3f2aec3243e61df7953c7cce6119cc47ecee0b24cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15430195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b0b68275de0a45def4867fb1881aa785677a0722159a1c4969813d6a3fea79`

```dockerfile
```

-	Layers:
	-	`sha256:cbf2b0094055661faad456ada789d2a0790671a5f5580e9b4cb82dd253a60a7e`  
		Last Modified: Sat, 22 Jun 2024 02:36:41 GMT  
		Size: 15.4 MB (15400528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475a6d30e99e6c9b2a7e20d88a9bb2f606e7433f59eeb0292a552313945673c0`  
		Last Modified: Sat, 22 Jun 2024 02:36:40 GMT  
		Size: 29.7 KB (29667 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:cbd19e828b353f265d67107d23b6339703e7d1e96bddd11af2f18b546f21b819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437727192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942ef25771e918daf8a955bd7f0e5e05010dd531e43092954f328157fa5d5e58`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:23 GMT
ADD file:ce7f1a42beaf6b57d9cd3b9b043cd6434d5b8da1315fee8cac2cd6fc2e7cc981 in / 
# Thu, 13 Jun 2024 00:48:24 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:13:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:15:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_VERSION=13.3.0
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:ba68704cd532bca61f763f11a4142906ee2aa565b2583052f6ddfff3fdf96b74`  
		Last Modified: Thu, 13 Jun 2024 00:51:14 GMT  
		Size: 47.3 MB (47338510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb056c8f4290f2ae7f12204b417f783b3346fe7fee14a5916fed571483b57f89`  
		Last Modified: Thu, 13 Jun 2024 01:24:01 GMT  
		Size: 22.7 MB (22728300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f981a74b01c05f914b1f13564a2cf75fc9471592be602f7b699412e5a62b8d`  
		Last Modified: Thu, 13 Jun 2024 01:24:23 GMT  
		Size: 61.5 MB (61517456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0475d9394b70464b90e234102b87625699171564d5f8cad8ec2f1d4de8fae2`  
		Last Modified: Thu, 13 Jun 2024 01:25:04 GMT  
		Size: 184.5 MB (184522344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b88039203776ce0791a987abc0c715cfa5aad59627f6d546240a88d5ad61a63`  
		Last Modified: Sat, 22 Jun 2024 03:42:43 GMT  
		Size: 2.7 MB (2710412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b95b22560c2cdcdaa073660e21cf9a56fc0223cab101446660444b6a6c2c2`  
		Last Modified: Sat, 22 Jun 2024 04:55:19 GMT  
		Size: 118.9 MB (118899101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8b66cad3dfa660c9f9c7de196ff809a3251d00e1c13c0aa72a38b42059bfc8`  
		Last Modified: Sat, 22 Jun 2024 04:55:16 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8f7ce80c0aab5ba3620273b13703b0ebd311d9f5df91c6b1c250d0c919b635`  
		Last Modified: Sat, 22 Jun 2024 04:55:16 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:281dbcf186b7f42201c01066ccbb6c7934fc167131ef0cbaa0ff44bc81d45239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15230700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9095256ce39c382565db7e501a9778dc13efde0165c671a1268d00059aa2d789`

```dockerfile
```

-	Layers:
	-	`sha256:69698dc26cd691d0aade80ebfbf481bb46c30d5922d26f114b6986da24bdd3c8`  
		Last Modified: Sat, 22 Jun 2024 04:55:16 GMT  
		Size: 15.2 MB (15200908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e4535034aa623af3e9851318e550978427587eafddc681e0c69b8d52f56ff7`  
		Last Modified: Sat, 22 Jun 2024 04:55:16 GMT  
		Size: 29.8 KB (29792 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:7cefa5427293368864980e6c02a19ca965fee3f057e07338edbef2a5eb4a685d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414631459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4ee4f1d7e55c056f1fb5eb7f405114349a1ec28eb28ef1cdf683508d9db1a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 May 2024 14:25:20 GMT
ADD file:4e983a5cb7d29543fc349746f45a7222e574dacf5a3c79841539a50f8c19121c in / 
# Tue, 21 May 2024 14:25:20 GMT
CMD ["bash"]
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:25:20 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 21 May 2024 14:25:20 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 21 May 2024 14:25:20 GMT
ENV GCC_VERSION=13.3.0
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:6f5c0eaba00958485596d442de72c808c288b19cb6598afa423aefa8c1c93274`  
		Last Modified: Thu, 13 Jun 2024 01:01:14 GMT  
		Size: 45.2 MB (45175040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43007e7b264595fb644d227437b5b5a40a08cf506f8905f388bee805d2e9ba`  
		Last Modified: Thu, 13 Jun 2024 01:33:04 GMT  
		Size: 22.0 MB (21953778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba09d7f8a9b10217e3ad0b9a640e8644b91701e59675c4e2443e6e4f8eb69c72`  
		Last Modified: Thu, 13 Jun 2024 01:33:24 GMT  
		Size: 59.2 MB (59217226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21d8970e0ba89fca18dc8a8432adc4570843d9db8e5e79d0ffb8099ce62748f`  
		Last Modified: Thu, 13 Jun 2024 01:34:03 GMT  
		Size: 175.2 MB (175175030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bac8ace9168ae3f462721afe7013d4e633d1c8a9847cf7ee573c2cb26e0b99a`  
		Last Modified: Thu, 13 Jun 2024 15:29:52 GMT  
		Size: 2.5 MB (2548577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503e2278558a7edd8631241dabc746d22cdf03c7851572ef31e12f1664c10a42`  
		Last Modified: Thu, 13 Jun 2024 16:36:43 GMT  
		Size: 110.6 MB (110550685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a4c73db72bddee29d667dc6df857542548435751debd1512542a80b8a54011`  
		Last Modified: Thu, 13 Jun 2024 16:36:40 GMT  
		Size: 9.3 KB (9334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff809629ac1326b2850179aa3eb75d88ac9f5be31dcb30f64967a61707bb2d3c`  
		Last Modified: Thu, 13 Jun 2024 16:36:40 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:aedd38eea1a63650cac06ccc5ec28bdf2817722f03e37c5ea7c8908b0ea6f8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15235869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07492d878aef576c969cdf7307627c15c266c0fd0b4b1c9451c44cf6c0b2970`

```dockerfile
```

-	Layers:
	-	`sha256:439e4ac2875df3561077536185d07b094b8b5a2c61790ebd7d0eb9adefa0895b`  
		Last Modified: Thu, 13 Jun 2024 16:36:41 GMT  
		Size: 15.2 MB (15206385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4b1d2f6fb999f6db12ae1e5f971d78a6b65edbba45c91a4c22a2bdbee86d7e`  
		Last Modified: Thu, 13 Jun 2024 16:36:40 GMT  
		Size: 29.5 KB (29484 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:445f23e000526c7941390cb697f667433f012f6d9824a5caf3e0e9587a4ae609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.4 MB (479357955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594bb6f81175741cd9c2418f64a7102945c406fde7d26e7794386cea73b3e91a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:22:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_VERSION=13.3.0
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dadad3edfd860d6d4fd52d4cbf17e7431a88d64161c62654786e60f331343a8`  
		Last Modified: Thu, 13 Jun 2024 01:30:17 GMT  
		Size: 23.6 MB (23586570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cd5f8f608f832afd85dc82fbac4aea05183fd7fccf555dd4a53a4bbe06b013`  
		Last Modified: Thu, 13 Jun 2024 01:30:33 GMT  
		Size: 64.0 MB (63994737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cb3bce424c387cc9f91f975242473b8be06d3426252fad4895105c051ad28`  
		Last Modified: Thu, 13 Jun 2024 01:31:02 GMT  
		Size: 202.6 MB (202593329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62f671e9439fe2ae33d52cd9272f92dda4b718bcac41d89a6196cfd83bb4306`  
		Last Modified: Sat, 22 Jun 2024 03:39:32 GMT  
		Size: 2.7 MB (2733602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e458082b60dc120673b509a3348e6fad1bb541ac428cc7862db1725ac16eb58e`  
		Last Modified: Sat, 22 Jun 2024 04:48:22 GMT  
		Size: 136.8 MB (136825069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53539851ad760b72c710507aacfa28f12f8b0586366ec41681d2237c9dbc98e`  
		Last Modified: Sat, 22 Jun 2024 04:48:18 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90698032fd2e67e6ecd44d313439eecb5f8132c51315508b088a9a424816abb`  
		Last Modified: Sat, 22 Jun 2024 04:48:19 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:2127ee0d5e4ee12db32c5bb8537cedbb81b792ea846d410a3d9555a709fbbab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15459113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0f3f0c7e1c8725b2ba6a40c0803892eed69ce2d7a4b42fd1cd921ef227279a`

```dockerfile
```

-	Layers:
	-	`sha256:6dd9582f4a7ab9e4f4c68689646f8af0ab30f65352b9368e98e07fc427866951`  
		Last Modified: Sat, 22 Jun 2024 04:48:19 GMT  
		Size: 15.4 MB (15429110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62e4a1fb9f3e4fedbf002944391683202aaf0285a3957d70ea94b7e3628341b`  
		Last Modified: Sat, 22 Jun 2024 04:48:18 GMT  
		Size: 30.0 KB (30003 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:e4aa8c871d0e00152f93f6cc3aa460ecf08793b5a574f46ffeb0e5b545cf05d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.6 MB (511634866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fab1d75dfe940370cbbbb541a82a4039aae45c819e7559d54d9c603261e38a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:16:47 GMT
ADD file:5b31953e08477fa1771514ef5fd326ae78b7c4ad417cbb64755ee493634ab392 in / 
# Thu, 13 Jun 2024 01:16:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:48:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		https://sourceware.org/pub/gcc/releases 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 20 Jun 2024 23:14:29 GMT
ENV GCC_VERSION=13.3.0
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Thu, 20 Jun 2024 23:14:29 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:7e04e800a5f6b106e3f1cb53c3677b55297b3841c160edc0f657f7a27ffb9ad0`  
		Last Modified: Thu, 13 Jun 2024 01:21:03 GMT  
		Size: 53.6 MB (53579678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4148242bae3618c54f03447132a7364c4a46c509d204908b4d8b569f2cbbf18d`  
		Last Modified: Thu, 13 Jun 2024 01:59:41 GMT  
		Size: 25.7 MB (25699643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0038ae14b2277791270ea7736f896040def15b2cfcc8a74ca0cfd14349e968`  
		Last Modified: Thu, 13 Jun 2024 02:00:03 GMT  
		Size: 69.6 MB (69583876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb32bd190e0cb532461d35afe27a691f4117106df93f8222c22c3c037b8b006`  
		Last Modified: Thu, 13 Jun 2024 02:00:56 GMT  
		Size: 214.2 MB (214235513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74426011cc73967468216c0c2f5ee3a80ea14a05af3b999354628467a901f54`  
		Last Modified: Thu, 13 Jun 2024 21:19:20 GMT  
		Size: 3.0 MB (2993543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51612da47b37035b38db4b293b8ef0457cb060b13002383d1961d2621b658440`  
		Last Modified: Sat, 22 Jun 2024 03:35:37 GMT  
		Size: 145.5 MB (145531305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c88c4012331d7897ae7a0c860e69b8dfe1c069f1ab4dd16e53bff4e8a575d99`  
		Last Modified: Sat, 22 Jun 2024 03:35:33 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2697a2d1ab1dd68a3302d419cccc4ac2da1c5c3f9aa51e2466dc3fe5c36a9563`  
		Last Modified: Sat, 22 Jun 2024 03:35:32 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:9fffb716938d04e0fdd9dc11d36000ef0ab89e21c487088cd619db1c14f8b3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15406951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d0646a0f7d18e5e68648f38207c3bb897d34880279a4f52f9bae6151d3bca0`

```dockerfile
```

-	Layers:
	-	`sha256:3d3c5861b02ef8fdf64bdb0ab0d5a83d1ea9411e2dec0b1fd37a6d7e27cc5249`  
		Last Modified: Sat, 22 Jun 2024 03:35:33 GMT  
		Size: 15.4 MB (15377228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049ad2654abba28bbfffa4ad6a481c42bd63c4c4cef09d0de6e814316cfd7778`  
		Last Modified: Sat, 22 Jun 2024 03:35:32 GMT  
		Size: 29.7 KB (29723 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:0395c00a67d01d96626f7c4e5e8543acb279293195e961c095da1bec71c93f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **469.9 MB (469869943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7aa820d6086e6de0cf21770a4e1499d3c4bf05a33a04eccccdabb9c8574b72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 May 2024 14:25:20 GMT
ADD file:4debdbf640f7b84de2c501cfcf8124343554f82fc2c8948149efc9e60c80c7f1 in / 
# Tue, 21 May 2024 14:25:20 GMT
CMD ["bash"]
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 May 2024 14:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		abigail-tools 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 May 2024 14:25:20 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Tue, 21 May 2024 14:25:20 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Tue, 21 May 2024 14:25:20 GMT
ENV GCC_VERSION=13.3.0
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	deb="$(readlink -ve /usr/lib/*/libstdc++.so* | head -1)"; 	gcc="$(readlink -ve /usr/local/lib*/libstdc++.so | head -1)"; 	LD_PRELOAD="$deb" abidiff --no-added-syms "$deb" "$gcc" # buildkit
# Tue, 21 May 2024 14:25:20 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:6d80f2b74ad971cfa89367f3157841bc726dd7cfbfd585d5aabbdac584178990`  
		Last Modified: Thu, 13 Jun 2024 00:47:26 GMT  
		Size: 47.9 MB (47942476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12a6c3cf967133a8f0a30b6c3f3b164be42f75e34007b370d4c4ccbbe04993`  
		Last Modified: Thu, 13 Jun 2024 05:30:54 GMT  
		Size: 24.0 MB (24046768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562db015b7d28466453e6548a5b0b491293d13e90bdeea148e63c5fe7b505321`  
		Last Modified: Thu, 13 Jun 2024 05:31:09 GMT  
		Size: 63.1 MB (63130173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c668b461560d605ae92dc415d62a300a7ad50f27d748de49478dea15f41cf594`  
		Last Modified: Thu, 13 Jun 2024 05:31:37 GMT  
		Size: 183.2 MB (183237091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20aa7a0677f99753fc10fa5456f67f18f46a7788fc28006001c5d77338c5c58b`  
		Last Modified: Thu, 13 Jun 2024 22:31:15 GMT  
		Size: 2.7 MB (2730059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b8e1909e81adbe6a457cd8effc9e8563b25a92f0275182198998b31c10c45e`  
		Last Modified: Fri, 14 Jun 2024 00:17:47 GMT  
		Size: 148.8 MB (148771699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fc385f61fa9fd8dab423baca3ef3c19514c5381f2a9753bbff1ffc7a506ef2`  
		Last Modified: Fri, 14 Jun 2024 00:17:45 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aed016581d9c3dfbfc1e174e85bc3c5be22123f7b8af723cd82205d42e857cb`  
		Last Modified: Fri, 14 Jun 2024 00:17:45 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:ddb562b7a97cac60e6c2ead5295696e8ba5d14d3e7ae008268b735e55112f902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15244566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c567793dacd7feda96bb066448c56146fa3c9829c8b552ce64d27788e69fa4da`

```dockerfile
```

-	Layers:
	-	`sha256:63dd9a9bdb955c695b19c4839e981992c87df576623b83fa52b1bbd7fee7f607`  
		Last Modified: Fri, 14 Jun 2024 00:17:45 GMT  
		Size: 15.2 MB (15215207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23686b9f1a247ffee12a6d103edde027cac42355ec0883fff20be59a64ea5e23`  
		Last Modified: Fri, 14 Jun 2024 00:17:45 GMT  
		Size: 29.4 KB (29359 bytes)  
		MIME: application/vnd.in-toto+json
