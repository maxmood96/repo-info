## `gcc:9-bullseye`

```console
$ docker pull gcc@sha256:6441c4fabea2f974839315211c9939b00a201d8ccc17f4230930227ceca28387
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

### `gcc:9-bullseye` - linux; amd64

```console
$ docker pull gcc@sha256:31aa108f2cafa2a83dcd23f29d3afe4fd87781a73e182f73a4aad18c3357508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.3 MB (421312812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d531ee799c1de7752750e7f179a0ae2e67b722350ad067e6b90e1a884edc8cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8975634c683a6a43240715f9554a329fa2702103694b2fabc72420b35b7da845`  
		Last Modified: Wed, 10 Apr 2024 07:54:46 GMT  
		Size: 98.9 MB (98872692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c6f9eb9bc39044d7df0b827c15dae107f477a9c0416753b9cfa141a36eee9f`  
		Last Modified: Wed, 10 Apr 2024 07:54:45 GMT  
		Size: 10.1 KB (10098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6e9c7484ca47a213569980bc467353556441e1890e4c5069bd0d1bdfecf7d`  
		Last Modified: Wed, 10 Apr 2024 07:54:45 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:0205ec8a41f4f3997266bae9bbc08f9153cff07d145a46869074b130678c90c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15001674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05cc8513abb3813f227faa44e5d45fc5c87995a7eed61ed4dfb0da70fa04236d`

```dockerfile
```

-	Layers:
	-	`sha256:b113bfb51e52768d66eda3a5f36dee698388a7c7dd634440ad742182e7c0995b`  
		Last Modified: Wed, 10 Apr 2024 07:54:45 GMT  
		Size: 15.0 MB (14974159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9cfd7ae3dee538114f14fe51fc7e33c1a234ccee14d54fbcad4c9fd59cace1`  
		Last Modified: Wed, 10 Apr 2024 07:54:45 GMT  
		Size: 27.5 KB (27515 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:9-bullseye` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b1acc896ab6f4d0ee9120bc5d00a3edcd15a16c4e2614ce218c640e3a611935d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379176699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b5eecb748e2a65570a794c62318e4ed0c7d5f742ef059d0a2a6a7ce8168e13`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2f143fe44237c686e570db73ca8e79a407a12cd45adcb3067acff6628c74a2`  
		Last Modified: Tue, 12 Mar 2024 01:45:14 GMT  
		Size: 175.2 MB (175154282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083936c85eaa93214cfa601bc392fd4f3607e080f1e9cf8f3d66fda1fc8ffb88`  
		Last Modified: Tue, 12 Mar 2024 14:44:43 GMT  
		Size: 83.7 MB (83720231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fd66e3becf7f188e7d24242fd5b68f8aef5c88cc01ffb7134d4e029070a04e`  
		Last Modified: Tue, 12 Mar 2024 14:44:41 GMT  
		Size: 9.8 KB (9842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eb3c50b60575db06314d6eb37ffb9ce518712d11c17a14318a799385206c89`  
		Last Modified: Tue, 12 Mar 2024 14:44:41 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:d52e78bd98d3baae5fb4b3696d465206ca746825958c0a0eb0c668d46bf75e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14797652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d77ad2ab8f42541663aad9fb9afa3b5f6bc6c0bf84e80180062f77deeb5d09f6`

```dockerfile
```

-	Layers:
	-	`sha256:8116d65ece28544c259dfc92f8033fcb024e194140948cb02ed8a1bf941a6e0c`  
		Last Modified: Tue, 12 Mar 2024 14:44:42 GMT  
		Size: 14.8 MB (14770690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f9275b65bda33e2cb84a357de6c732cc72508497c8b236e778390323879f567`  
		Last Modified: Tue, 12 Mar 2024 14:44:41 GMT  
		Size: 27.0 KB (26962 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:9-bullseye` - linux; arm variant v7

```console
$ docker pull gcc@sha256:008d8db88f29c90e2aa380ef48fa91f92025024fe42890d162da6b67b822b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361402846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a2d5356edbd0d52748e183baa652408e42c170e37b217682912b1102017a7e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43ced5929e1e21b0bb6da3fd4685c92c3a4732c60d389286438090b44f98663`  
		Last Modified: Wed, 13 Mar 2024 00:19:09 GMT  
		Size: 78.5 MB (78473673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2d7282ab3482e22b0efe6bc2124ae7cc0d8985f574975fe94cdec8ac8612e4`  
		Last Modified: Wed, 13 Mar 2024 00:19:07 GMT  
		Size: 9.9 KB (9900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddf6b79ac7468b54af08dc2ddd3857484bd94a801c073072e7c8c7632bdc2ea`  
		Last Modified: Wed, 13 Mar 2024 00:19:07 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:c5c8454b9b1435ff0fcd6bc34be33107bcb035e714a769c8f5a2de2000792d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14803026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868fac6b41e7a9c023a2e02b89fe77ecb8bdb9f8188e4746322026796b9538e0`

```dockerfile
```

-	Layers:
	-	`sha256:cb7edf99ba733c287bfe1125c6fe3fbf8453f1c0fcf71e42eae324a28b6b6b21`  
		Last Modified: Wed, 13 Mar 2024 00:19:07 GMT  
		Size: 14.8 MB (14776064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e28044cdbf62760835946214cabd18e6275de5457650485b300cb6c21bbe2c6e`  
		Last Modified: Wed, 13 Mar 2024 00:19:06 GMT  
		Size: 27.0 KB (26962 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:565151a0c964984d471f1445d5c4d6a559d8f82043d301730afa1fc4b21211ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400671968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102e796f3cddaefe23f5a394cf9c1528e4b6d7f2b6891187addeaf2722d49a15`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f68936b3673747c0e5f890171be43e7951f82b45f1a75c9d57585429cf306`  
		Last Modified: Thu, 11 Apr 2024 04:26:19 GMT  
		Size: 86.6 MB (86573193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658a799e9d9f618b6e635d94cc9f65a9e12274644f14570905e361180e40771b`  
		Last Modified: Thu, 11 Apr 2024 04:26:16 GMT  
		Size: 10.0 KB (10017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6479ec9f3c63781487b61370699a1fb86c2b0941c635d2ae17a903b2e4322130`  
		Last Modified: Thu, 11 Apr 2024 04:26:16 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:45ed89704eed91e055b193db8b62e0a391c06c8ca975de95e870dd4819214439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15003495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87025707e5925b3a92822cb44965a01129ff8e7a400d7b7dd6675c49a1d514e5`

```dockerfile
```

-	Layers:
	-	`sha256:48716e9887e2e2396a2858d12e1e6ae53365cbbce35e7de81ef75b6289c83449`  
		Last Modified: Thu, 11 Apr 2024 04:26:16 GMT  
		Size: 15.0 MB (14976629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a300f8fb8d5940dfc901320cc1a509134df536cef8899580102c75807efdbc`  
		Last Modified: Thu, 11 Apr 2024 04:26:15 GMT  
		Size: 26.9 KB (26866 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:9-bullseye` - linux; ppc64le

```console
$ docker pull gcc@sha256:b7e87662d692565498568a99dd5212f66d35c99013d9e4e1928fff3da73def58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.2 MB (429223132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c7ec9e95e95ddd4e1a9a883bf022ea1015b9134e4fc7b92a794b6b9bd05827`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:774dc7f7db45435bfddcc1ff7bb4ae0716252e8f7c3d074ff7611070207b8314 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:eed533dbdbda3df66dcde8a75fb0ab317466f575d116ffa4e053da66ab0dd942`  
		Last Modified: Wed, 10 Apr 2024 01:31:35 GMT  
		Size: 59.0 MB (58959030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e798a4c3c738ae3b2b3ae6f2b6f02c6db9d510fadd63004b60dd8268c907ee34`  
		Last Modified: Wed, 10 Apr 2024 07:17:41 GMT  
		Size: 16.8 MB (16765741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0da44da0fa59c2e0283157a263f65dcc5e2b22c7a5515c68bd6d82e305a55`  
		Last Modified: Wed, 10 Apr 2024 07:18:00 GMT  
		Size: 58.9 MB (58873011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cc15f136ce528a3936b4864554b8879c5d361f9d968ba9b756dd216f192eb`  
		Last Modified: Wed, 10 Apr 2024 07:18:39 GMT  
		Size: 196.3 MB (196345047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e4cc7cf5ae684f37c815807f231181a246e88a1b7450e3e38bfae08a26e428`  
		Last Modified: Thu, 11 Apr 2024 04:47:48 GMT  
		Size: 98.3 MB (98268319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1d8cbf712cce7fcb07023a804590372607d0c7af40ddbfae9d3992b8993706`  
		Last Modified: Thu, 11 Apr 2024 04:47:44 GMT  
		Size: 10.1 KB (10053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8bdedf281ef5d40ba6833ff09fec8ea3d6e222b9816608c3e3160475e885a1a`  
		Last Modified: Thu, 11 Apr 2024 04:47:44 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:55e0934923c47cc3f359e0430cb7a3e9d5868ec9eea332b6ca1f7603831762ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14970382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93fcc7546edb90bf385e2ea75e402fabe4ed26531d4fc49e5ab3864e81e3d5d`

```dockerfile
```

-	Layers:
	-	`sha256:8b06044d599e3aceaf3fdb3662705eccd8f6c21cf697f20b476a7c226918801b`  
		Last Modified: Thu, 11 Apr 2024 04:47:46 GMT  
		Size: 14.9 MB (14943476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac0f783683d015cad21affbd84670499b6de0a556d50f512a5458462924415e`  
		Last Modified: Thu, 11 Apr 2024 04:47:44 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:9-bullseye` - linux; s390x

```console
$ docker pull gcc@sha256:d28797d14e85faecb9b4a368b2c64d5870427c03f66f6f66a9718a642d346a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.0 MB (381016146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc583d54123d9a524251701b0e90182bd7264d877d608b61b70c1883e47be07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
# Fri, 27 Oct 2023 19:22:51 GMT
CMD ["bash"]
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 27 Oct 2023 19:22:51 GMT
ENV GCC_VERSION=9.5.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dbe74529fc57e85a22f94e3442e33e7b5d04e9a4e5bfef8746df1fd2841eb8`  
		Last Modified: Tue, 12 Mar 2024 02:49:00 GMT  
		Size: 173.0 MB (172991681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f737adcc81f8fc7ea20186548874bbcf056157813ebeeece8aad95d572720d0b`  
		Last Modified: Wed, 13 Mar 2024 11:52:22 GMT  
		Size: 85.0 MB (84975792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1cec967f4da22113ba30e24ed2b95d92cf2a8b8e28d50686a9a3abe408e8ab0`  
		Last Modified: Wed, 13 Mar 2024 11:52:20 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c731382b3b8d7f487171a77b2463e5cc4d356a1231d87173efaf6a1abb5891`  
		Last Modified: Wed, 13 Mar 2024 11:52:20 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:9-bullseye` - unknown; unknown

```console
$ docker pull gcc@sha256:538171aae609c1ddeeb8bbf481f63f594a6e45749b1eb24a3958f7563fee6d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14822687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a381de23aa71ba38a1b3af4d90cce418bf249f989009bee4c8dfb68ade77101`

```dockerfile
```

-	Layers:
	-	`sha256:c7ea61463ff888e26a50c384d7639cbb92b97bf612806711f01b929df6cc3f67`  
		Last Modified: Wed, 13 Mar 2024 11:52:21 GMT  
		Size: 14.8 MB (14795835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc159cab45a533198d15b048de3705873bdcee3721dc92e9a419f82bc9e5979`  
		Last Modified: Wed, 13 Mar 2024 11:52:20 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json
