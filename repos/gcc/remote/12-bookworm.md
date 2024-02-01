## `gcc:12-bookworm`

```console
$ docker pull gcc@sha256:6a0f2be6984802a6dee27cbfa68b125ee53bd64072b3092f9bcba48ef6281b94
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
$ docker pull gcc@sha256:51f14ed8fc7d1f61060e438f66a1427aba07a417d6d6d5aa90b00d4b7090d768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487731485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aced1743a24977ad3baf9735226bc1709465395761e6ee3138ca900442482c28`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991dd3dda70153eafc1ec661c0ce3bad23b2613aad2a0d5ac547213cabb49b76`  
		Last Modified: Thu, 01 Feb 2024 02:29:41 GMT  
		Size: 16.8 KB (16750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354320938ac44c3dfe1fc2364aaca54e8316d8fb54a9190ea5fbf554654c79e8`  
		Last Modified: Thu, 01 Feb 2024 02:29:44 GMT  
		Size: 138.8 MB (138815738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae242dc32b6ceaa737d42a761a0c31d7b59b2f557869856f6ada35a34f029f61`  
		Last Modified: Thu, 01 Feb 2024 02:29:41 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7998e0a75c1a7b039dcc24e1ea9a1d38e5a09805c19c8de7b5a0b0fd8106aa46`  
		Last Modified: Thu, 01 Feb 2024 02:29:41 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:b843b57f22465b2af3c4086bdaa3115a5780115d1de39e0906088e69056140df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13431804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7faa309f4b18f18852f9025ec551a4daf6cf16574092622bf0f3a6e309370931`

```dockerfile
```

-	Layers:
	-	`sha256:dd3d7be1be0f8389effc8fca71411370b1b492e436e2241223aeeb6816df246e`  
		Last Modified: Thu, 01 Feb 2024 02:29:41 GMT  
		Size: 13.4 MB (13401956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb52699b00aa1ed8ced5811797bfbd82522f1d12e639f6daadbd61b70f70ea2`  
		Last Modified: Thu, 01 Feb 2024 02:29:41 GMT  
		Size: 29.8 KB (29848 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:8669d0bb630ed30cd1e930bcf6549e4cc351a08f148c4497b568a4353b135bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427742161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558753447a0d9b32a664ad6e93d1f29c4a09da4ba7a3464b72010147dcfec216`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
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
	-	`sha256:151dd254612c1c98e4ecdda2e4e1be56cf21da0d68035ed661a4881af580027c`  
		Last Modified: Thu, 01 Feb 2024 06:54:46 GMT  
		Size: 16.8 KB (16761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad0ce2017f95ebb190cf681dd4340c2c95206f2f0ac532c666a06c5fd9f6a0`  
		Last Modified: Thu, 01 Feb 2024 09:32:49 GMT  
		Size: 111.7 MB (111703980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ab761cbd966cd79b1a52ed2e023021a9da79a1b464de1eedbaedab5cf26740`  
		Last Modified: Thu, 01 Feb 2024 09:32:45 GMT  
		Size: 9.2 KB (9232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b52e8f984e5921e3de1f11ad54f1074ffb4f9a824a3d634e1c97f67a937d54`  
		Last Modified: Thu, 01 Feb 2024 09:32:45 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:57fc3502dbbcfa1769ba4388b30ae8da7c284cf761daf800173d14920c940e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13256449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5bb92b2fe1b2b7e879b78adb6ae08cb30c4eff9d6fd510c702ad3e9ac92bc9`

```dockerfile
```

-	Layers:
	-	`sha256:8d170936a00359546bfd24808793f6c5d0a8cd3ecdc0a512533176a4ae29af59`  
		Last Modified: Thu, 01 Feb 2024 09:32:45 GMT  
		Size: 13.2 MB (13227138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e8fd390afe7ecf078f4fd47cded6ec6f8e8a56472c0b25909d4f8ca9f8cff30`  
		Last Modified: Thu, 01 Feb 2024 09:32:45 GMT  
		Size: 29.3 KB (29311 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:c250bcc27444020e6c4089f5e9323dc6bd427b001011b10bbf0a5b6502b01ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405081965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec126a15bc995671ef43eb4f38f6a2fc2937ee330a20f7ca4374f6eec3d74bd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4217895349d978f5d5f829a1b9f1d590307ed9bb5c0f7f995e80e9b2b82004f1`  
		Last Modified: Wed, 17 Jan 2024 02:18:53 GMT  
		Size: 59.2 MB (59213249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99d5ec604741fcefed97e18613277d558287884e80970d63c6c06d3079fea66`  
		Last Modified: Wed, 17 Jan 2024 02:19:38 GMT  
		Size: 175.1 MB (175075952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311ce2d6b487d650d89e67238b5a7dfe83dce5799e4136240517fdc28874dd7f`  
		Last Modified: Wed, 17 Jan 2024 17:02:32 GMT  
		Size: 16.8 KB (16763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8602850149e8d83cbfdadc2dbef69c8f73bf463a9cc27327c676e1ce3d195058`  
		Last Modified: Wed, 17 Jan 2024 19:17:04 GMT  
		Size: 103.7 MB (103658332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfa9d05c45a743d9c0ad2d7bb6a936433da6d579e8ca8b0a682e5919b44db92`  
		Last Modified: Wed, 17 Jan 2024 19:17:00 GMT  
		Size: 9.3 KB (9279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4495a2676b06e6e35e6b8f2e8396e450431b83cfb4fdf69018b95804995351c`  
		Last Modified: Wed, 17 Jan 2024 19:17:00 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:1a0139f2c17f2be6292f5abd25a6c906d9177ed4ab6ced0fd0b04d5a132797d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13260990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5951c0a2be4936c0e93b032059db36a60b7fe7763be01f31e4189102e60ea46`

```dockerfile
```

-	Layers:
	-	`sha256:4f43e47bad4b1f7965adb48ff553a1ee42724813e35e8e7ef4c53c57efc1c953`  
		Last Modified: Wed, 17 Jan 2024 19:17:01 GMT  
		Size: 13.2 MB (13231679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5b7ac547f0d35562988deea32d9c6034f484bad52b94418584560406132f6ea`  
		Last Modified: Wed, 17 Jan 2024 19:17:00 GMT  
		Size: 29.3 KB (29311 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:42274468742dc8b56667a846e19492b0e3269920e2f1ebbcad1c9f5bb7272118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.4 MB (465380628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3836233d19269b98899b21954496dfd79ea32c090e576f34c16c505d1b6e76d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b4f1810f998c1f1580e2404b2e7fed8e264902d898bbe531443ea9789b7641`  
		Last Modified: Wed, 17 Jan 2024 02:58:02 GMT  
		Size: 64.0 MB (63991147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c176cbf649709b5d8a03720a6c53e18e33ad50feef33abe83c5ae95c5aabdb2`  
		Last Modified: Wed, 17 Jan 2024 02:58:50 GMT  
		Size: 202.5 MB (202502448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ade2f0491a760634aecc41f7cc04138e2feaf58b4e16fa7389c4d20304e236`  
		Last Modified: Wed, 17 Jan 2024 19:23:09 GMT  
		Size: 16.8 KB (16762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeebd5a3e0e39f8f2a77e4e7d4548db99206beb75acd72adca749a74f6439ebb`  
		Last Modified: Wed, 17 Jan 2024 20:15:20 GMT  
		Size: 125.7 MB (125684173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ab63faad4227c7f1ad52e2e21003246520636a57bb8ad9f0ef5944ec14e1c0`  
		Last Modified: Wed, 17 Jan 2024 20:15:16 GMT  
		Size: 9.4 KB (9445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2616139502c6768494301a8c88cbd990f80c644cc638bb7564bcc09a33444`  
		Last Modified: Wed, 17 Jan 2024 20:15:16 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:8eddb9f341d74a720fba916d5459bbbb3669fae6cca268e9246024c649f786ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13456385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32f3fff4602a48cb6367dc10820e17d16bac0cddf9efdbc9ebe0ad558200b26`

```dockerfile
```

-	Layers:
	-	`sha256:0b8429678968fa65d8bd19d583e7acc43a5b296cca806ac4e7be3efdcd2c570b`  
		Last Modified: Wed, 17 Jan 2024 20:15:17 GMT  
		Size: 13.4 MB (13427185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2419287b8503f147cd32ac5f5c2d433f751e8adad181c2ffe98a0c794d4b2fc`  
		Last Modified: Wed, 17 Jan 2024 20:15:16 GMT  
		Size: 29.2 KB (29200 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:1c1be37004fe599ef8c7b84dfd15e1037574445362d21d70e5267d483919bad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 MB (498973345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7399f4eab00858d34491a2f21a2fa5f704d91fef04fd61e4231cc569c19051`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:181ff897280683d4e2f512551aa99c5bca9823305859ed4620c8ea3bd4d95cd5 in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:62296c33e75415de6ebf7e20132da876513ede04af94472801e60452c0a295dd`  
		Last Modified: Thu, 11 Jan 2024 02:38:58 GMT  
		Size: 53.6 MB (53557571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08c7f22c453d0296f7b3aac215dd01664f85d00e83a734e65de9f4669b9b11`  
		Last Modified: Thu, 11 Jan 2024 07:23:16 GMT  
		Size: 25.7 MB (25696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4b3bd26123c050bfca2111b37a82d4c385c67c129372b0688d3bea5051428`  
		Last Modified: Wed, 17 Jan 2024 03:24:46 GMT  
		Size: 69.6 MB (69581529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6b71c229676130f942ae91085124d04316997b949d1ba7a6500b460e2ce5ef`  
		Last Modified: Wed, 17 Jan 2024 03:25:28 GMT  
		Size: 214.1 MB (214137619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdf2cd0c92b851ab1f6adfe4629a9086ab98500587b3e30007f9a781b9ac64b`  
		Last Modified: Wed, 17 Jan 2024 15:09:41 GMT  
		Size: 16.8 KB (16754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb85f687df16ba85619aeae0248209bed40cd53bc8fccc45bf14c02365c4234`  
		Last Modified: Wed, 17 Jan 2024 15:58:28 GMT  
		Size: 136.0 MB (135972315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d54974a2e71a82401f4eb42e667e8b2aaf9910802226e7f4c23d6f73d7bc7f0`  
		Last Modified: Wed, 17 Jan 2024 15:58:24 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdee058693f064c1de043c4135108cd647e74b60d806c62b787073e7983e13d`  
		Last Modified: Wed, 17 Jan 2024 15:58:24 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:b47f9de9d30387573e948027c4f6f108a29a3fc35db38befc8b72e79a30914d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13411636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f20f57a3a6dcca1cfa7b08b2f5c49abed1969d746d264695c48873c76971a`

```dockerfile
```

-	Layers:
	-	`sha256:13683e7d8d91d4300ff034df6a104fef8044d72807e2ea8a24ba431a5a01a53f`  
		Last Modified: Wed, 17 Jan 2024 15:58:25 GMT  
		Size: 13.4 MB (13382395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bf80b44007497be0ed0d2e0adb04ccc4fa053f7df1096b9022d00139a7727bf`  
		Last Modified: Wed, 17 Jan 2024 15:58:24 GMT  
		Size: 29.2 KB (29241 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:6bc0398baa5a75299c5dd5d26e0cb8f47f6260b6a44284b2e6457646c2bf18e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.8 MB (435819557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae9f7df4f0745f76f1afdfbde407cee0421d1c6286d77f3ed8453d5a3007a1b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Jun 2023 21:54:01 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Wed, 21 Jun 2023 21:54:01 GMT
CMD ["bash"]
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06 	D3A93CAD751C2AF4F8C7AD516C35B99309B5FA62
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Wed, 21 Jun 2023 21:54:01 GMT
ENV GCC_VERSION=12.3.0
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Wed, 21 Jun 2023 21:54:01 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcda5a31401318d38b94cd36426844d1953c0561252561b5205f9b95c442bac`  
		Last Modified: Thu, 11 Jan 2024 02:21:00 GMT  
		Size: 24.0 MB (24043257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed6bc65286743fe499d9acd1b031ec55623990da97c0b8c5a36e90e5efb4f45`  
		Last Modified: Wed, 17 Jan 2024 04:03:37 GMT  
		Size: 63.1 MB (63126558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574246225f84293d825d33ddedfe60c69bf6ec125be2de566f07c54ea8e0e2f2`  
		Last Modified: Wed, 17 Jan 2024 04:04:05 GMT  
		Size: 183.1 MB (183143910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524329aabfc6f82da82038e1ef859f4a636848d51b969225fe37b6768214b91`  
		Last Modified: Thu, 18 Jan 2024 06:08:59 GMT  
		Size: 16.7 KB (16734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010b3686b0e44067e548e22e59759b4abdb8c3e656470738bc675ff0f3f610eb`  
		Last Modified: Thu, 18 Jan 2024 08:22:11 GMT  
		Size: 117.6 MB (117559654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9dbc5ad434f623c9a93135618179b19a758a1fc2894eae78b0a382b23edb7`  
		Last Modified: Thu, 18 Jan 2024 08:22:08 GMT  
		Size: 9.8 KB (9768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a1a6767e641681a5125bd88888fa858c9a08fc96db26b1ef71dce8450ec0dc`  
		Last Modified: Thu, 18 Jan 2024 08:22:08 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f01f81d85c40b92b82a2f70b70d1f0709700348645c187b4b76bef3e893c0565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13267242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bee0f478a90b35ea1058ec578206018763a711dcaeec70e866873f8a0bcb2c`

```dockerfile
```

-	Layers:
	-	`sha256:f70dcefc777d50e9fd203cce3d73b4e5b0335e392431a1e633153537cdbdc910`  
		Last Modified: Thu, 18 Jan 2024 08:22:09 GMT  
		Size: 13.2 MB (13238056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d049173f51888fd6e990286bb1952ec90af38eb331898c02fb579df1ad3c7f5`  
		Last Modified: Thu, 18 Jan 2024 08:22:08 GMT  
		Size: 29.2 KB (29186 bytes)  
		MIME: application/vnd.in-toto+json
