## `gcc:13-bookworm`

```console
$ docker pull gcc@sha256:699e417d1e5d7f50a0aeb348c0d58543b96f480ed08a947f02939559538f6b25
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
$ docker pull gcc@sha256:a349d67f77aba4e801fdf56bd18baeb6c37c9197dd06d49605dd74702e09f8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.9 MB (493908798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdce34a93dae8da071983a57d5f5de2223340fa293c4d42d8ebd2539cc8554c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c558fac597f8ecbb7a66712e14912ce1d83b23a92ca8b6ff14eef209ab01aff2`  
		Last Modified: Tue, 13 Feb 2024 01:31:35 GMT  
		Size: 211.1 MB (211120435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ab4737a454a17b248eed44f3e276c6279e281b707b46b11dd0d55687784b2a`  
		Last Modified: Tue, 13 Feb 2024 04:37:54 GMT  
		Size: 145.0 MB (145037486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1739d98eacad36e9d480ad7d60e59c99e9eafd383d287f619c77175de93007`  
		Last Modified: Tue, 13 Feb 2024 04:37:50 GMT  
		Size: 9.6 KB (9575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7b11b5dc3364bc0160f27b96e0d0f281d78aecc57da2cce5ee6851c109df3c`  
		Last Modified: Tue, 13 Feb 2024 04:37:50 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:387b87461abf064000565e273acc8f4e07ca20517bf655160ec2704c52278fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13430832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f187c6d480fdb93573cc90e34ee40e4716f73972c2b14581a7229f3376d141a`

```dockerfile
```

-	Layers:
	-	`sha256:570aeff9b7a533fea5775a20b3efa998edc33c70dadc7099e118e4569c397503`  
		Last Modified: Tue, 13 Feb 2024 04:37:51 GMT  
		Size: 13.4 MB (13402600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3812e918259cbef785aeeafbb699912a188ab7299043e3d6b60457b2dc42fa`  
		Last Modified: Tue, 13 Feb 2024 04:37:50 GMT  
		Size: 28.2 KB (28232 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:ac559c96d73e07b7aa87bde7da6e57f1cb98a355154ea10d66843a6c68352ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.6 MB (434578486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0994f23ea0ddda3129ad7e38e0623538ca1d06a02db2edc2cbbc683acb10220a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad25eb5c49c8ee60b2f9c576ab52c62fdeeae27d9d0aff4526469c55fa65ac`  
		Last Modified: Wed, 31 Jan 2024 23:23:36 GMT  
		Size: 184.4 MB (184421840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1c8b138e67902319b6dcad91a995b08655530a11e22cf3f42fc64324de95a2`  
		Last Modified: Fri, 02 Feb 2024 02:42:42 GMT  
		Size: 118.6 MB (118557063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a277017b7af20900d7a0bead8f588c277c6c5293e403473566a959fdeb6e0aa4`  
		Last Modified: Fri, 02 Feb 2024 02:42:38 GMT  
		Size: 9.2 KB (9230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2adb505147b630ad7dda0b1604da33fcb5fac22a3cd21da1731980a900831`  
		Last Modified: Fri, 02 Feb 2024 02:42:39 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:60a9af630398782612314c74714e4b0d55d225ab0ba3a0f6d3b49dc6cfb9facb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13255439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ff1a24b34cb8a7ef78e51776b96af5a1b9e9e62708a2a213815322bdd7ee08`

```dockerfile
```

-	Layers:
	-	`sha256:8b4b3e7d0450c2773c6dad7fc6afd5cc797baf2e0f6f714c6440cbc77f0fce40`  
		Last Modified: Fri, 02 Feb 2024 02:42:39 GMT  
		Size: 13.2 MB (13227742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a67e080dd9a96a70cc24bf25a83f2bf82884a9d909486e1e3f51b07c1789eb9`  
		Last Modified: Fri, 02 Feb 2024 02:42:38 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:b8950d97d2a6264381384200eaab7f7263b02dcbef99ae3374621f35f9b5f286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411646736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13f32769df578e8ad9a8a5bdeaffe71f94d4aa011c4966792a1a187f18dcee2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1784359581b4acfe38c3643d3ecc7f33e782e5cf24d981e4d5e74ac155134548`  
		Last Modified: Fri, 02 Feb 2024 21:32:46 GMT  
		Size: 110.2 MB (110205461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc883aff4881383554b1d056e532f6f9a7cfd1fb5b38fc62cb33c9ff6a62a75`  
		Last Modified: Fri, 02 Feb 2024 21:32:43 GMT  
		Size: 9.2 KB (9231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a82b94d8c01139976bb8d0747cadf2ee4940264c80738747d9c95dc4dcda2d`  
		Last Modified: Fri, 02 Feb 2024 21:32:43 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:051d563f4c620fdc862693f3a9fffea876c0ae3bc4c0bf3e921554f5bed601cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13260914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3980e99584e194f08a304ce405bf8055ecd0cc3c581538a13e51fd91327aa5a`

```dockerfile
```

-	Layers:
	-	`sha256:bed647c941c3217b9e38149ba3b098e47f4395e927e40a716d1687e840f5413c`  
		Last Modified: Fri, 02 Feb 2024 21:32:45 GMT  
		Size: 13.2 MB (13233216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:148ea76c9d0c8e582e5ebf90670a4cae4b42ffb506037a4e046cbd3de7f33c61`  
		Last Modified: Fri, 02 Feb 2024 21:32:42 GMT  
		Size: 27.7 KB (27698 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:59297809509f77bbb0ab97b4c2aa2b839ee87b17ba3a63e7e06e0279ea9a9085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.2 MB (476174816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e047910772bbdb95335f53cffaa378f7415f175dd48af0e8e2eed1c285cfabd3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcabfc6c415bdafce0fb78b78afe51a8be789b05c4c3f5ccf5f1046bb5d32776`  
		Last Modified: Tue, 13 Feb 2024 01:47:24 GMT  
		Size: 202.5 MB (202519692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf82be3973d3b6d3e46aa2e63e200d9336c2f4c2ab7bc3cd228d6afb9a6c240`  
		Last Modified: Tue, 13 Feb 2024 18:39:26 GMT  
		Size: 136.5 MB (136479299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57091aad3370c1c657e29336e5f4ef689af9d6eed885fde9b5a097d0b15b967`  
		Last Modified: Tue, 13 Feb 2024 18:39:23 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa1b813c0be423e86613f0fff733662b77bc0372a2d77ebba35f0833dc18fd0`  
		Last Modified: Tue, 13 Feb 2024 18:39:23 GMT  
		Size: 1.8 KB (1800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:6f4329cdfc244c99891b9bd36b281e0a2993961e87b0249f7da36ca58ec7867a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13456084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23734b9992e6b2196b7b7b3755757d029b6f543d067b8dcd08b5378f83a820a5`

```dockerfile
```

-	Layers:
	-	`sha256:def3fec3a4c6f190be5944b345869d9a0964ac0dac7d3f7f2ebf66365dd78914`  
		Last Modified: Tue, 13 Feb 2024 18:39:21 GMT  
		Size: 13.4 MB (13427833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e526d8e5695cd2a779aa5172c874f1e0ffc368ed22e6f5f56d850d9a7762e4e`  
		Last Modified: Tue, 13 Feb 2024 18:39:21 GMT  
		Size: 28.3 KB (28251 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:ca451a50a5c5f8db38f4d50ed7c7434b3c5c37019a6f1264d462735bf2599ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.1 MB (508095700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed99383e5f6cca6711fc2435fa7dafa526347bdea29099b191da5e077763db7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4766a6e0e49a985c19ff5bed265467d9f1f6eada575066cf5a142c50bd88a57d`  
		Last Modified: Tue, 13 Feb 2024 07:37:13 GMT  
		Size: 214.2 MB (214151358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2b8dcf240c16fcad27e41d8706de775dcc3bbc1f305fea238ad5beda5283`  
		Last Modified: Tue, 13 Feb 2024 17:19:03 GMT  
		Size: 145.1 MB (145099115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66066bba177f0be6bd3dbc99befc8bf58630a8496d07f61320fcf43eada32dd`  
		Last Modified: Tue, 13 Feb 2024 17:18:59 GMT  
		Size: 9.4 KB (9383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c46a73f879cd279ea6fd81099634d82ce90fa65eae3702dfe86a41141c6ce1`  
		Last Modified: Tue, 13 Feb 2024 17:19:00 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:da97cddbd777bcc1826f7e80fed90f8b1aded4c3214df5c3536ce8dccfbd1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13412283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d3fc47b888e91755b91afe90ac5f059a5e7e903cba3bc837d889e4a8d8a81c`

```dockerfile
```

-	Layers:
	-	`sha256:c52bd425e00dc711e8a0458d0a3ce0ebee0a13c4a3279a9072801e39133b823e`  
		Last Modified: Tue, 13 Feb 2024 17:18:56 GMT  
		Size: 13.4 MB (13383984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999ed646233a8b866ca6d2d2bf19b5862f7a399a3407a3395845e295a6c02957`  
		Last Modified: Tue, 13 Feb 2024 17:18:55 GMT  
		Size: 28.3 KB (28299 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:13-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:d436dbd8d4cc84475c5ba1af1524939741020df24e7dc5d68b8ce15ecfeee0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.6 MB (466633467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aae3f88f566dfa91e9855b997ea0c56ca012cf6aa2080d58e0e82dec3c5ce13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=13.2.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fbf38c964e08de060948c059512a46ce00a75cb6793f2d8193ebd5f461c00f`  
		Last Modified: Thu, 08 Feb 2024 04:43:59 GMT  
		Size: 148.4 MB (148355973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99b043a51fd30c39bc14b9bbda3c0c68be8d7f20b238796ce18b93cbcc6c5c7`  
		Last Modified: Thu, 08 Feb 2024 04:43:55 GMT  
		Size: 9.7 KB (9735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fafa6698e7d41cecf6d9952af2a540d0ff58d8dc86fa043c63111fd9fb2d83`  
		Last Modified: Thu, 08 Feb 2024 04:43:55 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:13-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:0320e8bf505253ac652698fbba8978802abfe6457a7e749f7de8526b4d02721a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13266214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbead4bf3db4663a885c540474ffc0be53bdd39e428e33905bfde6fa12bac686`

```dockerfile
```

-	Layers:
	-	`sha256:a9bc05b393b72fc8b3b31e1eebc7591df4536ee94c07a53ad41fc826d2d0c42c`  
		Last Modified: Thu, 08 Feb 2024 04:43:55 GMT  
		Size: 13.2 MB (13238644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b4f0ec562aef4ee95aec2f59f193bf44608c69834f55f88c5f862f1ca0f24e`  
		Last Modified: Thu, 08 Feb 2024 04:43:55 GMT  
		Size: 27.6 KB (27570 bytes)  
		MIME: application/vnd.in-toto+json
