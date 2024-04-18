## `gcc:12-bookworm`

```console
$ docker pull gcc@sha256:aa35938ababe3efc6980d2c502c8ea1e58e928d03a997bcfeaf94474e56cf61b
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
$ docker pull gcc@sha256:db4fe52c99a3a571394607ed444114c2eebcfa5cd1a7d217693f9f6d6a1613c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **487.7 MB (487712540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f97e2051ece8216ce51eb689266d2856e49ae8f3724fdd3e5221a7ada15bdbe`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0ef63d6c3dc228cdae09434da44a661d016cf67483c86ebd7475bdfce1e0a6`  
		Last Modified: Wed, 10 Apr 2024 08:25:36 GMT  
		Size: 138.8 MB (138815750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad5dfb72f38e9641155382d7e04dc7f2f439515ccb9045cf6e4d9e0a757f42d`  
		Last Modified: Wed, 10 Apr 2024 08:25:31 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d50482ce1138b39bbbf81ce16eab2a63d667214414c3dd4a032bb2ffd1c7315`  
		Last Modified: Wed, 10 Apr 2024 08:25:31 GMT  
		Size: 1.8 KB (1791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:e74b86dba502fb9defb8cf519dfb59ddcc658c29c9c96548d850075392fa9d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15396400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f8997d19223a483ba470e13629dd5698ce1511bc0d75dc6ee25412509ee9fb`

```dockerfile
```

-	Layers:
	-	`sha256:24eb09a8a90750f9e51c6e5bbbecc49d9f9db2d5d6223cebfade5db89346ef81`  
		Last Modified: Wed, 10 Apr 2024 08:25:32 GMT  
		Size: 15.4 MB (15368755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae4edd0e7fe3adb41ba6c4e59b51541ac5b20d3bd8a3556ff9bd0eb4a6e20115`  
		Last Modified: Wed, 10 Apr 2024 08:25:31 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v5

```console
$ docker pull gcc@sha256:ac4e19b4fca5b5d815eb4cca09af9466ac8f109510bcaa948b4b1116ca463735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427727776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a673ed77d2fa3788c931f489725855bf4f3c1b01112b8f36def5622cd12a1e6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:b0965dc0b90d6c10055f9e01eee401939303a005eff01dfc0ac17671ac10c89e in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:db9b031fc6f21cd210f5feeda489a6e10c26355e778fbdaeca7ec9da4a730942`  
		Last Modified: Wed, 10 Apr 2024 00:54:05 GMT  
		Size: 47.3 MB (47316142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ffbd9696eb657ee7a1f58c3ba55b7068e9217f964a268f6c9f74a7dd54e30c`  
		Last Modified: Wed, 10 Apr 2024 04:55:15 GMT  
		Size: 22.7 MB (22725022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a129a04f2d6b83a7f3a316a17496ec1b1a884022ea93fc33decc4cb7520e38`  
		Last Modified: Wed, 10 Apr 2024 04:55:38 GMT  
		Size: 61.5 MB (61515822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf0e0e8befd59b55c6a9b9cab341b48b4727d523d5b2d09b7e6f1948f4682ca`  
		Last Modified: Wed, 10 Apr 2024 04:56:17 GMT  
		Size: 184.5 MB (184456802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68be6f436757bcb5e2fc3d909c9b65631283f36df9ab1fa65b675cb6a2d668`  
		Last Modified: Thu, 11 Apr 2024 02:58:19 GMT  
		Size: 111.7 MB (111702983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94d9d3c6e97c678160d3040c744b84a6b946f3ddc797b4db9e83bb710ea4461`  
		Last Modified: Thu, 11 Apr 2024 02:58:15 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513b72c6017a9699fa97da5fa7ca96001be7802dc944b9ae1d2308fe4364323d`  
		Last Modified: Thu, 11 Apr 2024 02:58:15 GMT  
		Size: 1.8 KB (1797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:5cac3cdbf8d28e9611f5d52dc93078c07e6bcf020ead5c144978a68822a8663e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15196227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85473eea6c480d3dbdae1b06d717d83cc63b73b120d5c77e1ce601b2939d2bf6`

```dockerfile
```

-	Layers:
	-	`sha256:ace950eb0b18c2641c39223dd629e094e713a2f8020815a7342c821b3caa2dbd`  
		Last Modified: Thu, 11 Apr 2024 02:58:16 GMT  
		Size: 15.2 MB (15169133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b9ca804477bd5e0757e11c146ccf25815dfd0218973b40aa83a22ea5169a70`  
		Last Modified: Thu, 11 Apr 2024 02:58:15 GMT  
		Size: 27.1 KB (27094 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm variant v7

```console
$ docker pull gcc@sha256:b8012ff1a3984ddd1a0c17bed928b6e49d0823775da8537df757a3d8bcba4e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.1 MB (405092941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f410cb72bd544078f12d83b99a1d74df6f3820e9f06710af3bdd308697838b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c7a8d13f1cb4d9563e860774594263654335ea2632429095932fd3c26aa69e`  
		Last Modified: Fri, 12 Apr 2024 04:45:55 GMT  
		Size: 103.7 MB (103656048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0545e11f93cd6a9e61090ae06b686f28933e5524f188e4875a36dc30ce798`  
		Last Modified: Fri, 12 Apr 2024 04:45:52 GMT  
		Size: 9.2 KB (9243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c029dc5ca3b562df5db087d4b8c2736a10992ef6b1e208ab22c308682dae92`  
		Last Modified: Fri, 12 Apr 2024 04:45:52 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:f9531114a54e553966322bf91f54947bbfddad427695ffb65e819602302b5479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15201701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ad3ee79c0a3390dc32b9af49a8c5c4de8024d7888089b8ad60195158f2c35e`

```dockerfile
```

-	Layers:
	-	`sha256:7daff7f2778fc090ac7abf3fbc062604a2530ccc03a2a89f6c4eae76a3bfc473`  
		Last Modified: Fri, 12 Apr 2024 04:45:52 GMT  
		Size: 15.2 MB (15174607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0594b9bed542550d3586eafa1122e91b655c4e27b0c5329b2f72e3580976b9`  
		Last Modified: Fri, 12 Apr 2024 04:45:52 GMT  
		Size: 27.1 KB (27094 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:3c17397a1cc6846e511138e7283129f1d7e6c7c8dfe74f54ccd363e0e9f20f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.4 MB (465404297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667cbe904d53cae7fee4f1438f086ca519f5a398e4a78df27c0a9860e5ab62c5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38feb8224494380e40a98c43cc4d77c6de03c6797d02d0b92d3c26446e2e4fa`  
		Last Modified: Thu, 11 Apr 2024 01:15:33 GMT  
		Size: 125.7 MB (125684609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1402b366ada9bfbd776d2ea7ef4c2519101f0138f7a8acb8802e2b226ac69`  
		Last Modified: Thu, 11 Apr 2024 01:15:30 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bc1407472db84dc8cc61330d19187d543a6ceddc21f4f3475106feb577f263`  
		Last Modified: Thu, 11 Apr 2024 01:15:30 GMT  
		Size: 1.8 KB (1795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:74cc1563b970c957313a2b9dc7dcc0a834855de3bf477e9c8d9bc4dc5bc9e9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15424266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bdb1ab513e9dd5fcd8e072f1d1b980558c69d11557c9d136c6f94081ed043d`

```dockerfile
```

-	Layers:
	-	`sha256:3b9ba56c290bf3033c2b13f1865fe2ba2c3fae447e8b867b5708925ef439599f`  
		Last Modified: Thu, 11 Apr 2024 01:15:31 GMT  
		Size: 15.4 MB (15397270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d6647aad66082d0d2d1d54811d4547c051fee17356c17661d1d4953641c46f`  
		Last Modified: Thu, 11 Apr 2024 01:15:30 GMT  
		Size: 27.0 KB (26996 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; ppc64le

```console
$ docker pull gcc@sha256:de307839e93f3b447cbb58d865211b8caae16df2da4379e7e03b7003ff9f2bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.0 MB (498996795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4ef3370615b729304d741ef2e0148378d11f585ffc198788188110a1f815bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0dede385435598179e3ab86d7c4094cf59880d986b82c837b42b0649d5afa`  
		Last Modified: Wed, 10 Apr 2024 07:17:27 GMT  
		Size: 214.2 MB (214172353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a3eb3307f37bfad73ab0d352a43feb6acb54892cede13039346e54dbc7c0a`  
		Last Modified: Thu, 11 Apr 2024 02:22:04 GMT  
		Size: 136.0 MB (135973027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704e6e1886a7de1cf18a09ff80bc4d70e3cbd461d8eb0ba92a72815c4fdd8a1`  
		Last Modified: Thu, 11 Apr 2024 02:22:00 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9138bed70db3d3619d322193de4dfd64d813297fae5d078f387849d46f58efc`  
		Last Modified: Thu, 11 Apr 2024 02:22:00 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:61db4820c43a6042261d9d6f7584eaadb8ca0a674d5269066cb9b9c03f10df94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15372477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0f7fc5a687df5066ebfa65feec489050f230959c0e45034d3852b2989a7bb7`

```dockerfile
```

-	Layers:
	-	`sha256:58ed56c6d291876eb3ef50cfe4b440d2963864a0ea5d61ce147632742677a5bb`  
		Last Modified: Thu, 11 Apr 2024 02:22:00 GMT  
		Size: 15.3 MB (15345441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e87cecdaec9c97a0e06024b869cd9460f0e740d31ee4b85cabdee1c7ccdc47f`  
		Last Modified: Thu, 11 Apr 2024 02:21:59 GMT  
		Size: 27.0 KB (27036 bytes)  
		MIME: application/vnd.in-toto+json

### `gcc:12-bookworm` - linux; s390x

```console
$ docker pull gcc@sha256:930e32726588e0cbf4d147694220cb04b7b57090726a7c3c3ff4071ad6c97ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.8 MB (435830847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa2ee34a0465c7ac041c188f52dcb726a46aacb4386bd0a4947780339738f8f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Oct 2023 19:22:51 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
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
ENV GCC_VERSION=12.3.0
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 		gnupg 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv5te --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a+fp --with-float=hard --with-mode=thumb" 			;; 				i386) 			extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686"; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	{ echo '/usr/local/lib64'; echo '/usr/local/lib'; } > /etc/ld.so.conf.d/000-local-lib.conf; 	ldconfig -v; 	bash -Eeuo pipefail -xc ' 		deb="$(strings /usr/lib/*/libstdc++.so* | grep "^GLIBC" | sort -u)"; 		gcc="$(strings /usr/local/lib*/libstdc++.so | grep "^GLIBC" | sort -u)"; 		diff="$(comm -23 <(cat <<<"$deb") <(cat <<<"$gcc"))"; 		test -z "$diff"; 	' # buildkit
# Fri, 27 Oct 2023 19:22:51 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999 # buildkit
```

-	Layers:
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a94fdcea32a650c77c01028838d670a5840f3ead5a1cf5526e922967f0df66`  
		Last Modified: Wed, 10 Apr 2024 07:30:52 GMT  
		Size: 24.0 MB (24043531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec0019454e24574ad418259f50f0d68508dcf92f31f05ca5d5ad33dcf43bb`  
		Last Modified: Wed, 10 Apr 2024 07:31:10 GMT  
		Size: 63.1 MB (63126889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfce7e73c441e81b6b2408dea6732c47c87f4c633b91c6d77faf8891b50ab262`  
		Last Modified: Wed, 10 Apr 2024 07:31:45 GMT  
		Size: 183.2 MB (183165967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73b9158ac096788d6e237adf8f0abd72126ec0e564a3d69271ed489e738d90b`  
		Last Modified: Fri, 12 Apr 2024 10:52:22 GMT  
		Size: 117.6 MB (117560075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc064ef8691b0bb327521d963cd34abc52e2db4804c746dacf24c742b2cfd92b`  
		Last Modified: Fri, 12 Apr 2024 10:52:20 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfd02be93ab16f15bbb8a08df254d5fe000ac59ae3aa1b3e4df4aafe25b246f`  
		Last Modified: Fri, 12 Apr 2024 10:52:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gcc:12-bookworm` - unknown; unknown

```console
$ docker pull gcc@sha256:339d9bfada66c7f789f455404788fc8883003037707d46b0910e364abe5178e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15210425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed9a8a7078ba36e09be7b7411e9c2b3fe28b063ef265d4c11680957c3f5c33f`

```dockerfile
```

-	Layers:
	-	`sha256:40244eab6532c4b65ea8f544d70a0e824fbf6620330db7f5d9ada111c26caa9a`  
		Last Modified: Fri, 12 Apr 2024 10:52:21 GMT  
		Size: 15.2 MB (15183443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66ae51db1903d72f4cdfac4caf047b9934cfe5041fc6b9387b50994c8821ef93`  
		Last Modified: Fri, 12 Apr 2024 10:52:20 GMT  
		Size: 27.0 KB (26982 bytes)  
		MIME: application/vnd.in-toto+json
