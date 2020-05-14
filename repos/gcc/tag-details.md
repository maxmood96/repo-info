<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gcc`

-	[`gcc:10`](#gcc10)
-	[`gcc:10.1`](#gcc101)
-	[`gcc:10.1.0`](#gcc1010)
-	[`gcc:8`](#gcc8)
-	[`gcc:8.4`](#gcc84)
-	[`gcc:8.4.0`](#gcc840)
-	[`gcc:9`](#gcc9)
-	[`gcc:9.3`](#gcc93)
-	[`gcc:9.3.0`](#gcc930)
-	[`gcc:latest`](#gcclatest)

## `gcc:10`

```console
$ docker pull gcc@sha256:d77a3324ee4cf7313139c92d3f35bcade17214105bf5ee924bc0f284550e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:10` - linux; amd64

```console
$ docker pull gcc@sha256:81f3c9bedf3de5722fbcb3a381ed0e17c6d365d374e0fe863a61c6a6a0780c7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (428977935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba82d803294cfecf3eeda9e93f2758c9ea0cb15b2e967b229ae91192178a92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:52:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:52:51 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:52:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cc6130165afdb489e362815df100adf022784cac64b5bf6d913e8bba4483`  
		Last Modified: Fri, 08 May 2020 22:53:33 GMT  
		Size: 116.8 MB (116765792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1833f92a59cbed26f01e520cccacb1fe0fb9714309fc3ca3882acbca0f9433`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 11.5 KB (11549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a93c7b003c9fc5379bcc0cf63959b4bc96cbffd53dc57a8e5446242216b07`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 1.9 KB (1922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10` - linux; arm variant v5

```console
$ docker pull gcc@sha256:67568420cc3b4590ca3c87267130d47657b070bc622dcb571ec205c7dd8dea69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384043551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f46631b9df67c6251ec9897c9a19619b70d53361ac1e81d8d833b68f4d78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:00:58 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:02:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:02:08 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:02:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2596fc4b427c0db2a100a6d8710b133dd8fc5d6b4b9aff45eb744126fb55`  
		Last Modified: Thu, 14 May 2020 19:49:12 GMT  
		Size: 98.1 MB (98127258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badfd4878178afb0ea124ffce701ab81db28035fbdc316eee16199b335294ad5`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.1 KB (11129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c2b0594177e11ab085897a4cfac99e2c2521eeb90487bdaa9fc6a8588b5a13`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10` - linux; arm variant v7

```console
$ docker pull gcc@sha256:185830f370ea6119e3e171931de533a99ab97b83bb458388087c001efe7425c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368869580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21abb6ce5b250900c0df757d4704ae59cbd1bf27c88dd3337d7fe4270d644ed0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:01:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:01:49 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:01:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39cf71475197cb803e8f333c9a4c5aa313a9a761a6a95f5a5889b72ce50eec3`  
		Last Modified: Thu, 14 May 2020 19:42:58 GMT  
		Size: 90.8 MB (90758908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3b1129091b11584ef1685c216e7f790cd9824db10206b4af9bebb57dbeb461`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.2 KB (11181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c2f56f8399d1b07c4fb52c8e06d4567a6a16b319a230d806115ba110d211e`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:d44dc0fcf57df5713d3a35f5808e4ed330a5e9addd87759e9993537176d6bc9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411611201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095d30119b6f5c555dc139e92220d731606bce5111170ef39e89d8c60f869a3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:36 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:54:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:54:36 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:54:39 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1fe54daeaf31c9b21837b776e36801220de4e4caa338fa903a4bb593c10295`  
		Last Modified: Thu, 14 May 2020 19:25:36 GMT  
		Size: 108.9 MB (108855097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffc610427070ffb0ddfb754cc1685c509ec2039b55edaaaa4e8027b47b1211`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ba3bb67de421a577c388fae447ccf001189416578da6e72432c9177f18915`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10` - linux; ppc64le

```console
$ docker pull gcc@sha256:f437cbec3fd8f3330609480bfcd82e22f84fdddf2232c2378ed999dd109ca78d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453132519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3b2aceb0055eadd7e56eb43b15de9a10d42cd37fdcc05e072ad1dbd82a3e0e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:17:31 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:25:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:25:45 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:26:00 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d594e861f679a0e38d19b8fe060dcf02374c4d1774350e40b5b2f042482322`  
		Last Modified: Fri, 08 May 2020 21:39:10 GMT  
		Size: 119.5 MB (119545345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7925dfdd35263e8a915953d765f0919b897526b9f09dbc6d1ef33cb089369`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565b9b6bb59c98fa31c654ce2123bbbb9eec00f2db832cd4fb1e7e6df1ec1c78`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10` - linux; s390x

```console
$ docker pull gcc@sha256:2e17a91b3ee6e18fcd83f6e016bd69f8eab8a151f7feba9584d4d2571176924e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394838634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdecee948c99042005977042455fb9b640f3e1ea649ef8a586948f121d81897`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:53:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:53:55 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:53:56 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df604c60fd52716f44861b5c9cd7e7170413a449dbf7a2ca434d2f112ed1a3a3`  
		Last Modified: Thu, 14 May 2020 19:44:30 GMT  
		Size: 100.5 MB (100451895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000b3e8df7d91b0e25950beb75592431163c7fcd629953ebf853dccf0f7eb2e`  
		Last Modified: Thu, 14 May 2020 19:44:28 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ae588af340eb12f25c24bead1d2981fb2b2d30b64f187bf2aba679b072a8c`  
		Last Modified: Thu, 14 May 2020 19:44:29 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:10.1`

```console
$ docker pull gcc@sha256:d77a3324ee4cf7313139c92d3f35bcade17214105bf5ee924bc0f284550e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:10.1` - linux; amd64

```console
$ docker pull gcc@sha256:81f3c9bedf3de5722fbcb3a381ed0e17c6d365d374e0fe863a61c6a6a0780c7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (428977935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba82d803294cfecf3eeda9e93f2758c9ea0cb15b2e967b229ae91192178a92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:52:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:52:51 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:52:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cc6130165afdb489e362815df100adf022784cac64b5bf6d913e8bba4483`  
		Last Modified: Fri, 08 May 2020 22:53:33 GMT  
		Size: 116.8 MB (116765792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1833f92a59cbed26f01e520cccacb1fe0fb9714309fc3ca3882acbca0f9433`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 11.5 KB (11549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a93c7b003c9fc5379bcc0cf63959b4bc96cbffd53dc57a8e5446242216b07`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 1.9 KB (1922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1` - linux; arm variant v5

```console
$ docker pull gcc@sha256:67568420cc3b4590ca3c87267130d47657b070bc622dcb571ec205c7dd8dea69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384043551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f46631b9df67c6251ec9897c9a19619b70d53361ac1e81d8d833b68f4d78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:00:58 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:02:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:02:08 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:02:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2596fc4b427c0db2a100a6d8710b133dd8fc5d6b4b9aff45eb744126fb55`  
		Last Modified: Thu, 14 May 2020 19:49:12 GMT  
		Size: 98.1 MB (98127258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badfd4878178afb0ea124ffce701ab81db28035fbdc316eee16199b335294ad5`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.1 KB (11129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c2b0594177e11ab085897a4cfac99e2c2521eeb90487bdaa9fc6a8588b5a13`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1` - linux; arm variant v7

```console
$ docker pull gcc@sha256:185830f370ea6119e3e171931de533a99ab97b83bb458388087c001efe7425c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368869580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21abb6ce5b250900c0df757d4704ae59cbd1bf27c88dd3337d7fe4270d644ed0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:01:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:01:49 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:01:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39cf71475197cb803e8f333c9a4c5aa313a9a761a6a95f5a5889b72ce50eec3`  
		Last Modified: Thu, 14 May 2020 19:42:58 GMT  
		Size: 90.8 MB (90758908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3b1129091b11584ef1685c216e7f790cd9824db10206b4af9bebb57dbeb461`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.2 KB (11181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c2f56f8399d1b07c4fb52c8e06d4567a6a16b319a230d806115ba110d211e`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:d44dc0fcf57df5713d3a35f5808e4ed330a5e9addd87759e9993537176d6bc9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411611201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095d30119b6f5c555dc139e92220d731606bce5111170ef39e89d8c60f869a3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:36 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:54:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:54:36 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:54:39 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1fe54daeaf31c9b21837b776e36801220de4e4caa338fa903a4bb593c10295`  
		Last Modified: Thu, 14 May 2020 19:25:36 GMT  
		Size: 108.9 MB (108855097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffc610427070ffb0ddfb754cc1685c509ec2039b55edaaaa4e8027b47b1211`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ba3bb67de421a577c388fae447ccf001189416578da6e72432c9177f18915`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1` - linux; ppc64le

```console
$ docker pull gcc@sha256:f437cbec3fd8f3330609480bfcd82e22f84fdddf2232c2378ed999dd109ca78d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453132519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3b2aceb0055eadd7e56eb43b15de9a10d42cd37fdcc05e072ad1dbd82a3e0e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:17:31 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:25:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:25:45 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:26:00 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d594e861f679a0e38d19b8fe060dcf02374c4d1774350e40b5b2f042482322`  
		Last Modified: Fri, 08 May 2020 21:39:10 GMT  
		Size: 119.5 MB (119545345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7925dfdd35263e8a915953d765f0919b897526b9f09dbc6d1ef33cb089369`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565b9b6bb59c98fa31c654ce2123bbbb9eec00f2db832cd4fb1e7e6df1ec1c78`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1` - linux; s390x

```console
$ docker pull gcc@sha256:2e17a91b3ee6e18fcd83f6e016bd69f8eab8a151f7feba9584d4d2571176924e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394838634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdecee948c99042005977042455fb9b640f3e1ea649ef8a586948f121d81897`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:53:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:53:55 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:53:56 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df604c60fd52716f44861b5c9cd7e7170413a449dbf7a2ca434d2f112ed1a3a3`  
		Last Modified: Thu, 14 May 2020 19:44:30 GMT  
		Size: 100.5 MB (100451895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000b3e8df7d91b0e25950beb75592431163c7fcd629953ebf853dccf0f7eb2e`  
		Last Modified: Thu, 14 May 2020 19:44:28 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ae588af340eb12f25c24bead1d2981fb2b2d30b64f187bf2aba679b072a8c`  
		Last Modified: Thu, 14 May 2020 19:44:29 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:10.1.0`

```console
$ docker pull gcc@sha256:d77a3324ee4cf7313139c92d3f35bcade17214105bf5ee924bc0f284550e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:10.1.0` - linux; amd64

```console
$ docker pull gcc@sha256:81f3c9bedf3de5722fbcb3a381ed0e17c6d365d374e0fe863a61c6a6a0780c7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (428977935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba82d803294cfecf3eeda9e93f2758c9ea0cb15b2e967b229ae91192178a92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:52:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:52:51 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:52:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cc6130165afdb489e362815df100adf022784cac64b5bf6d913e8bba4483`  
		Last Modified: Fri, 08 May 2020 22:53:33 GMT  
		Size: 116.8 MB (116765792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1833f92a59cbed26f01e520cccacb1fe0fb9714309fc3ca3882acbca0f9433`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 11.5 KB (11549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a93c7b003c9fc5379bcc0cf63959b4bc96cbffd53dc57a8e5446242216b07`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 1.9 KB (1922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:67568420cc3b4590ca3c87267130d47657b070bc622dcb571ec205c7dd8dea69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384043551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f46631b9df67c6251ec9897c9a19619b70d53361ac1e81d8d833b68f4d78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:00:58 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:02:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:02:08 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:02:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2596fc4b427c0db2a100a6d8710b133dd8fc5d6b4b9aff45eb744126fb55`  
		Last Modified: Thu, 14 May 2020 19:49:12 GMT  
		Size: 98.1 MB (98127258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badfd4878178afb0ea124ffce701ab81db28035fbdc316eee16199b335294ad5`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.1 KB (11129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c2b0594177e11ab085897a4cfac99e2c2521eeb90487bdaa9fc6a8588b5a13`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:185830f370ea6119e3e171931de533a99ab97b83bb458388087c001efe7425c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368869580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21abb6ce5b250900c0df757d4704ae59cbd1bf27c88dd3337d7fe4270d644ed0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:01:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:01:49 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:01:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39cf71475197cb803e8f333c9a4c5aa313a9a761a6a95f5a5889b72ce50eec3`  
		Last Modified: Thu, 14 May 2020 19:42:58 GMT  
		Size: 90.8 MB (90758908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3b1129091b11584ef1685c216e7f790cd9824db10206b4af9bebb57dbeb461`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.2 KB (11181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c2f56f8399d1b07c4fb52c8e06d4567a6a16b319a230d806115ba110d211e`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:d44dc0fcf57df5713d3a35f5808e4ed330a5e9addd87759e9993537176d6bc9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411611201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095d30119b6f5c555dc139e92220d731606bce5111170ef39e89d8c60f869a3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:36 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:54:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:54:36 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:54:39 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1fe54daeaf31c9b21837b776e36801220de4e4caa338fa903a4bb593c10295`  
		Last Modified: Thu, 14 May 2020 19:25:36 GMT  
		Size: 108.9 MB (108855097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffc610427070ffb0ddfb754cc1685c509ec2039b55edaaaa4e8027b47b1211`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ba3bb67de421a577c388fae447ccf001189416578da6e72432c9177f18915`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:f437cbec3fd8f3330609480bfcd82e22f84fdddf2232c2378ed999dd109ca78d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453132519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3b2aceb0055eadd7e56eb43b15de9a10d42cd37fdcc05e072ad1dbd82a3e0e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:17:31 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:25:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:25:45 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:26:00 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d594e861f679a0e38d19b8fe060dcf02374c4d1774350e40b5b2f042482322`  
		Last Modified: Fri, 08 May 2020 21:39:10 GMT  
		Size: 119.5 MB (119545345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7925dfdd35263e8a915953d765f0919b897526b9f09dbc6d1ef33cb089369`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565b9b6bb59c98fa31c654ce2123bbbb9eec00f2db832cd4fb1e7e6df1ec1c78`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:10.1.0` - linux; s390x

```console
$ docker pull gcc@sha256:2e17a91b3ee6e18fcd83f6e016bd69f8eab8a151f7feba9584d4d2571176924e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394838634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdecee948c99042005977042455fb9b640f3e1ea649ef8a586948f121d81897`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:53:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:53:55 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:53:56 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df604c60fd52716f44861b5c9cd7e7170413a449dbf7a2ca434d2f112ed1a3a3`  
		Last Modified: Thu, 14 May 2020 19:44:30 GMT  
		Size: 100.5 MB (100451895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000b3e8df7d91b0e25950beb75592431163c7fcd629953ebf853dccf0f7eb2e`  
		Last Modified: Thu, 14 May 2020 19:44:28 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ae588af340eb12f25c24bead1d2981fb2b2d30b64f187bf2aba679b072a8c`  
		Last Modified: Thu, 14 May 2020 19:44:29 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:8`

```console
$ docker pull gcc@sha256:9ec76f3becf379ffd376a602428ddad1b1c6fe822c093ed5eeb673bd08729137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:8` - linux; amd64

```console
$ docker pull gcc@sha256:0074f9ad2916e13541a4b0f38acf132bfa435d981c4944dc6eab02ea9e495ef9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408257955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9575f45cfbce85f5da57848eb22a2730df7d232cfee9fc0dcb9e3c115a8c875`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 21:18:14 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 22:52:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 22:52:53 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 22:52:54 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46b78a110a9cd60150477e25459fa427ae54dce04bc2b5ee384e6233e600db`  
		Last Modified: Fri, 08 May 2020 22:54:23 GMT  
		Size: 96.0 MB (96045730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c69756601869a0e64962f12ae27230bbe5055ba99b0ec68e5ae1263ec033f1`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 11.6 KB (11622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8fa27632573222a6292591c4ac0780df06db88e50cac9ff2ffd6507ff8a93`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b7dc5976c015cb1a494ebab3bbf2d3655c7ac63b9a5fe1aadf6ccb42835dc25b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367100206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0a84127fd66df226493537cef57c6894176a0081c9723c6fd72ab2bc4d68d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:55:47 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:48:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:48:10 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:48:14 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead96459fdaf6a0b59a12f65c6afef93a135cf18398c38296227af02ff8e471`  
		Last Modified: Thu, 14 May 2020 19:50:31 GMT  
		Size: 81.2 MB (81183922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cc87e11f4116f1adf2570698d9651ac55be405e6878c55796a16ddf2eed159`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 11.1 KB (11120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e28cd77af32c254c1ad99e00c27f0788d91bb644a2820b1914218a34ae63b06`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8` - linux; arm variant v7

```console
$ docker pull gcc@sha256:3a27f0be70cdebb1399c3becc4e296db8eecfaea9b32b80ee82ee408d75354a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353814303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7b350b07f6de9c2a21945359dc9482c6b2c276fbf3107d7c2c8dd37122cb2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:51:59 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:42:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:42:09 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:42:13 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5afd7643267f1dfff502ed9fe75ecb0f70143ce2fc3bcda6f1bcf28021b4f4`  
		Last Modified: Thu, 14 May 2020 19:44:12 GMT  
		Size: 75.7 MB (75703645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537c4bcb551f06d414c1fe16d75cb8609ddc4af730b05198d8594b9b29a6a50`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 11.2 KB (11171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1a03a2686a5bc11e1bd4ab5894c2de614c0fb73312bbd9b40d82d679b07e84`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:e42b91227ba848d29781f1695f2f7e1364b328b435c2576ee31b2a3947bf78c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a496abbda06f744d3781244f59ea093e947279913aea7e24c0af833ef07d2d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:39:56 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:24:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:24:38 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:24:40 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696dfb07b67875299de1906d0af0555fea36dc440b5c1fd6a3ee8282cc910b2`  
		Last Modified: Thu, 14 May 2020 19:26:51 GMT  
		Size: 83.1 MB (83147288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14665843d9a52cd8291a815a6fd0329ba6f6a0cd1b631931c2fb28b760f72904`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e431ed0a2d1f39f388716f53a8537d9055efecea1fffffe8ec69a1779c18f1`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8` - linux; ppc64le

```console
$ docker pull gcc@sha256:cddd8978194c9834cc662b5bdc0d58db577fae9c28ab3c797d255d81c3a57add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430600404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be3a2871075c9ab5e4b00054af9195990a007dcd9390b74d6a36abf73fc8547`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 20:28:01 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 21:37:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:37:17 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:37:28 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c00bb8b2fdd1ec98b87cf4bae8184c978b686b5d372c8a286b7e7c15604a8`  
		Last Modified: Fri, 08 May 2020 21:40:44 GMT  
		Size: 97.0 MB (97013229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07f6b268ccb3f152306d041ecdcdefb8fbd307eb714526e23884cc673982e55`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 11.5 KB (11493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce36597bbe5f4b028b3c564f339e6180e09357133fb0d450d7229d957a3ebe4`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8` - linux; s390x

```console
$ docker pull gcc@sha256:e69c1861b726e6d3b82da4638b16328b686c60ce8a0fc061cea9448bb315fa4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376925757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ba39ccfd7dc43973a9d2dbc6d2c8dd31d71877120f540c40d8979a5339082e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:46:49 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:43:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b02425d34392a37f9d0a607a3f44ac4b34ed3840734b3a34262e680b48c7767`  
		Last Modified: Thu, 14 May 2020 19:45:29 GMT  
		Size: 82.5 MB (82539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fc66d958fa03b129b7cbfadb36a128233f849ba38b178aa6d84ff346c5c4c`  
		Last Modified: Thu, 14 May 2020 19:45:16 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7111e4d96ca448dc20e57ea428c56afade57ca2718cb36b4fc5079ffcde26c`  
		Last Modified: Thu, 14 May 2020 19:45:15 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:8.4`

```console
$ docker pull gcc@sha256:9ec76f3becf379ffd376a602428ddad1b1c6fe822c093ed5eeb673bd08729137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:8.4` - linux; amd64

```console
$ docker pull gcc@sha256:0074f9ad2916e13541a4b0f38acf132bfa435d981c4944dc6eab02ea9e495ef9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408257955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9575f45cfbce85f5da57848eb22a2730df7d232cfee9fc0dcb9e3c115a8c875`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 21:18:14 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 22:52:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 22:52:53 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 22:52:54 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46b78a110a9cd60150477e25459fa427ae54dce04bc2b5ee384e6233e600db`  
		Last Modified: Fri, 08 May 2020 22:54:23 GMT  
		Size: 96.0 MB (96045730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c69756601869a0e64962f12ae27230bbe5055ba99b0ec68e5ae1263ec033f1`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 11.6 KB (11622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8fa27632573222a6292591c4ac0780df06db88e50cac9ff2ffd6507ff8a93`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b7dc5976c015cb1a494ebab3bbf2d3655c7ac63b9a5fe1aadf6ccb42835dc25b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367100206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0a84127fd66df226493537cef57c6894176a0081c9723c6fd72ab2bc4d68d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:55:47 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:48:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:48:10 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:48:14 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead96459fdaf6a0b59a12f65c6afef93a135cf18398c38296227af02ff8e471`  
		Last Modified: Thu, 14 May 2020 19:50:31 GMT  
		Size: 81.2 MB (81183922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cc87e11f4116f1adf2570698d9651ac55be405e6878c55796a16ddf2eed159`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 11.1 KB (11120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e28cd77af32c254c1ad99e00c27f0788d91bb644a2820b1914218a34ae63b06`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4` - linux; arm variant v7

```console
$ docker pull gcc@sha256:3a27f0be70cdebb1399c3becc4e296db8eecfaea9b32b80ee82ee408d75354a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353814303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7b350b07f6de9c2a21945359dc9482c6b2c276fbf3107d7c2c8dd37122cb2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:51:59 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:42:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:42:09 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:42:13 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5afd7643267f1dfff502ed9fe75ecb0f70143ce2fc3bcda6f1bcf28021b4f4`  
		Last Modified: Thu, 14 May 2020 19:44:12 GMT  
		Size: 75.7 MB (75703645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537c4bcb551f06d414c1fe16d75cb8609ddc4af730b05198d8594b9b29a6a50`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 11.2 KB (11171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1a03a2686a5bc11e1bd4ab5894c2de614c0fb73312bbd9b40d82d679b07e84`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:e42b91227ba848d29781f1695f2f7e1364b328b435c2576ee31b2a3947bf78c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a496abbda06f744d3781244f59ea093e947279913aea7e24c0af833ef07d2d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:39:56 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:24:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:24:38 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:24:40 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696dfb07b67875299de1906d0af0555fea36dc440b5c1fd6a3ee8282cc910b2`  
		Last Modified: Thu, 14 May 2020 19:26:51 GMT  
		Size: 83.1 MB (83147288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14665843d9a52cd8291a815a6fd0329ba6f6a0cd1b631931c2fb28b760f72904`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e431ed0a2d1f39f388716f53a8537d9055efecea1fffffe8ec69a1779c18f1`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4` - linux; ppc64le

```console
$ docker pull gcc@sha256:cddd8978194c9834cc662b5bdc0d58db577fae9c28ab3c797d255d81c3a57add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430600404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be3a2871075c9ab5e4b00054af9195990a007dcd9390b74d6a36abf73fc8547`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 20:28:01 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 21:37:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:37:17 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:37:28 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c00bb8b2fdd1ec98b87cf4bae8184c978b686b5d372c8a286b7e7c15604a8`  
		Last Modified: Fri, 08 May 2020 21:40:44 GMT  
		Size: 97.0 MB (97013229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07f6b268ccb3f152306d041ecdcdefb8fbd307eb714526e23884cc673982e55`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 11.5 KB (11493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce36597bbe5f4b028b3c564f339e6180e09357133fb0d450d7229d957a3ebe4`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4` - linux; s390x

```console
$ docker pull gcc@sha256:e69c1861b726e6d3b82da4638b16328b686c60ce8a0fc061cea9448bb315fa4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376925757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ba39ccfd7dc43973a9d2dbc6d2c8dd31d71877120f540c40d8979a5339082e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:46:49 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:43:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b02425d34392a37f9d0a607a3f44ac4b34ed3840734b3a34262e680b48c7767`  
		Last Modified: Thu, 14 May 2020 19:45:29 GMT  
		Size: 82.5 MB (82539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fc66d958fa03b129b7cbfadb36a128233f849ba38b178aa6d84ff346c5c4c`  
		Last Modified: Thu, 14 May 2020 19:45:16 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7111e4d96ca448dc20e57ea428c56afade57ca2718cb36b4fc5079ffcde26c`  
		Last Modified: Thu, 14 May 2020 19:45:15 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:8.4.0`

```console
$ docker pull gcc@sha256:9ec76f3becf379ffd376a602428ddad1b1c6fe822c093ed5eeb673bd08729137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:8.4.0` - linux; amd64

```console
$ docker pull gcc@sha256:0074f9ad2916e13541a4b0f38acf132bfa435d981c4944dc6eab02ea9e495ef9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408257955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9575f45cfbce85f5da57848eb22a2730df7d232cfee9fc0dcb9e3c115a8c875`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 21:18:14 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 22:52:52 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 22:52:53 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 22:52:54 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf46b78a110a9cd60150477e25459fa427ae54dce04bc2b5ee384e6233e600db`  
		Last Modified: Fri, 08 May 2020 22:54:23 GMT  
		Size: 96.0 MB (96045730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c69756601869a0e64962f12ae27230bbe5055ba99b0ec68e5ae1263ec033f1`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 11.6 KB (11622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8fa27632573222a6292591c4ac0780df06db88e50cac9ff2ffd6507ff8a93`  
		Last Modified: Fri, 08 May 2020 22:54:05 GMT  
		Size: 1.9 KB (1931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:b7dc5976c015cb1a494ebab3bbf2d3655c7ac63b9a5fe1aadf6ccb42835dc25b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367100206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0a84127fd66df226493537cef57c6894176a0081c9723c6fd72ab2bc4d68d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:55:47 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:48:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:48:10 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:48:14 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dead96459fdaf6a0b59a12f65c6afef93a135cf18398c38296227af02ff8e471`  
		Last Modified: Thu, 14 May 2020 19:50:31 GMT  
		Size: 81.2 MB (81183922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cc87e11f4116f1adf2570698d9651ac55be405e6878c55796a16ddf2eed159`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 11.1 KB (11120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e28cd77af32c254c1ad99e00c27f0788d91bb644a2820b1914218a34ae63b06`  
		Last Modified: Thu, 14 May 2020 19:50:04 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:3a27f0be70cdebb1399c3becc4e296db8eecfaea9b32b80ee82ee408d75354a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353814303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7b350b07f6de9c2a21945359dc9482c6b2c276fbf3107d7c2c8dd37122cb2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:51:59 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:42:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:42:09 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:42:13 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5afd7643267f1dfff502ed9fe75ecb0f70143ce2fc3bcda6f1bcf28021b4f4`  
		Last Modified: Thu, 14 May 2020 19:44:12 GMT  
		Size: 75.7 MB (75703645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537c4bcb551f06d414c1fe16d75cb8609ddc4af730b05198d8594b9b29a6a50`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 11.2 KB (11171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1a03a2686a5bc11e1bd4ab5894c2de614c0fb73312bbd9b40d82d679b07e84`  
		Last Modified: Thu, 14 May 2020 19:43:47 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:e42b91227ba848d29781f1695f2f7e1364b328b435c2576ee31b2a3947bf78c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.9 MB (385903396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a496abbda06f744d3781244f59ea093e947279913aea7e24c0af833ef07d2d0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:39:56 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:24:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:24:38 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:24:40 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7696dfb07b67875299de1906d0af0555fea36dc440b5c1fd6a3ee8282cc910b2`  
		Last Modified: Thu, 14 May 2020 19:26:51 GMT  
		Size: 83.1 MB (83147288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14665843d9a52cd8291a815a6fd0329ba6f6a0cd1b631931c2fb28b760f72904`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e431ed0a2d1f39f388716f53a8537d9055efecea1fffffe8ec69a1779c18f1`  
		Last Modified: Thu, 14 May 2020 19:26:24 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:cddd8978194c9834cc662b5bdc0d58db577fae9c28ab3c797d255d81c3a57add
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.6 MB (430600404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be3a2871075c9ab5e4b00054af9195990a007dcd9390b74d6a36abf73fc8547`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 20:28:01 GMT
ENV GCC_VERSION=8.4.0
# Fri, 08 May 2020 21:37:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:37:17 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:37:28 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0c00bb8b2fdd1ec98b87cf4bae8184c978b686b5d372c8a286b7e7c15604a8`  
		Last Modified: Fri, 08 May 2020 21:40:44 GMT  
		Size: 97.0 MB (97013229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07f6b268ccb3f152306d041ecdcdefb8fbd307eb714526e23884cc673982e55`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 11.5 KB (11493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce36597bbe5f4b028b3c564f339e6180e09357133fb0d450d7229d957a3ebe4`  
		Last Modified: Fri, 08 May 2020 21:40:20 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:8.4.0` - linux; s390x

```console
$ docker pull gcc@sha256:e69c1861b726e6d3b82da4638b16328b686c60ce8a0fc061cea9448bb315fa4c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.9 MB (376925757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ba39ccfd7dc43973a9d2dbc6d2c8dd31d71877120f540c40d8979a5339082e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:46:49 GMT
ENV GCC_VERSION=8.4.0
# Thu, 14 May 2020 19:43:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 19:44:02 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b02425d34392a37f9d0a607a3f44ac4b34ed3840734b3a34262e680b48c7767`  
		Last Modified: Thu, 14 May 2020 19:45:29 GMT  
		Size: 82.5 MB (82539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9fc66d958fa03b129b7cbfadb36a128233f849ba38b178aa6d84ff346c5c4c`  
		Last Modified: Thu, 14 May 2020 19:45:16 GMT  
		Size: 11.7 KB (11690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7111e4d96ca448dc20e57ea428c56afade57ca2718cb36b4fc5079ffcde26c`  
		Last Modified: Thu, 14 May 2020 19:45:15 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:9`

```console
$ docker pull gcc@sha256:616391d848f730d1153684a657303345189597c73a521db0723d5942c42f9196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:9` - linux; amd64

```console
$ docker pull gcc@sha256:043d094a7723cc594215b6accc93cb5f1a217d8afe15047265813a7aebe61ab1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.2 MB (411205415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147dcea158c509870804ccb4c32b7d2268b992f35578203db28837bb4a953cdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:53:04 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 21:17:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:17:57 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:17:58 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b48ca60a82e649783056a8bae6eb8894f16e9775b956a750d51a8a78b5cf3f6`  
		Last Modified: Fri, 08 May 2020 22:54:00 GMT  
		Size: 99.0 MB (98993282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14840e2d1ee496e332c24ce56076a530cb924ba9fb42f35f8c9f0cd30999b4b8`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60089f3984928cfb6171261431dc2199a2ba290bd0b42f4239c934914cce866`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 1.9 KB (1927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9` - linux; arm variant v5

```console
$ docker pull gcc@sha256:4a127d8dcd95fe4bf75f0b96b99c16c21921658451e64e2b6f3303bf20ec71e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369946764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91db00d1d7e215e3f8b89c1fdf2e83f8a7ba7dd31e1be1f94b740128e87b30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:40 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:55:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:55:16 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:55:24 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21447cdb103b079f031307a67f8409e2651baec69f1e51dfd30255356db742d`  
		Last Modified: Thu, 14 May 2020 19:49:56 GMT  
		Size: 84.0 MB (84030481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c8f6d309b6e617dfb4a2dc8008e41b92cf4f12d050955bc33932882de9c9c`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 11.1 KB (11117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf23ae33bdcf5ffdf077b58da736691a306ba623feaa9c4be3993eaed750fa4`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9` - linux; arm variant v7

```console
$ docker pull gcc@sha256:e8467839029bf8145f92b2e123b284187d6a4de9b8ed92fd1bf37e4cb7fcd8fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356703087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803c01f3a15f3ae26e343569892e37fa35953d995da072342efe846699e85a38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:10 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:51:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:51:42 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:51:44 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b26f0ab624e98b8a36880b0e83d19aa9ff313dd5bb0ea2664a4d1e5d8eb2c`  
		Last Modified: Thu, 14 May 2020 19:43:40 GMT  
		Size: 78.6 MB (78592437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82a31e49dd2a244459f157d0afeaf3b5cfd11aea809587fcf12c8583c4d3d69`  
		Last Modified: Thu, 14 May 2020 19:43:07 GMT  
		Size: 11.2 KB (11164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497fc4fbeae3398bee3e76d69dbbc527d55b35f8caceb73dd58859517f4fe19f`  
		Last Modified: Thu, 14 May 2020 19:43:08 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:82b319e3bc433bdc55947c08d514642cb8f61a13a0488275a979e02ef4c6e35a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389278867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25390cfc43d97393ff7fcadcabad238de565470beb9b49f81d16f7a6306bfcfc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:57 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:39:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:39:31 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:39:36 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab669a79249fe8768e08ec233fa7d37c230231da4f6a51f1c564896d14ea3a`  
		Last Modified: Thu, 14 May 2020 19:26:15 GMT  
		Size: 86.5 MB (86522753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad5dd4dfd4c2eeb29f2a2a09a5e46515e5089fbb5c014ce6fda8d69ecfd712`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0292db9e2ccacc650379d717d8cb7b52d111de11c85366c144fd5e6ab83864ef`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9` - linux; ppc64le

```console
$ docker pull gcc@sha256:c706c303b604d83a9b993b175e90d83ef5a37798191a4e64d313cfed4153a187
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.9 MB (431907706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe19dcf35542b3fa03589d13f8d66a11403eaaeb8d33eb01220ef615c737ffe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:27:26 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 20:27:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 20:27:41 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 20:27:47 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a51c27ed7ab734bd4b8836d4989c4e5a045e734cc343dfb22441fca350046`  
		Last Modified: Fri, 08 May 2020 21:40:07 GMT  
		Size: 98.3 MB (98320532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb3ce2c02f01b638a3e9dd6461104e646bc12e2e46f177e8df3fee7e538f13a`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 11.5 KB (11492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c23823132d98a1a06ccc1d9a36b95841809cf92647694dbc240d5587de97840`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9` - linux; s390x

```console
$ docker pull gcc@sha256:ee68155d8a1b2ba81adaa9cd1df17dbc0f9862dfcfda003af488a14ccb64a3a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379468746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9c9379480e41ed171cff59be783300f2a5ff8a7e22af3f774e9d147dd28b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:03 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:46:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:46:40 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:46:41 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee759df493092067547375bcd535956243a61200ff99c1652e15326e07d9b89`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 85.1 MB (85082005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b21a03c089d2af3f5415db551c8845665fad6b9a079343b362d614104430967`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 11.7 KB (11700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2795547afe67b0d409222d9ccecb43cabe8d76f42c57d39efdf8cf28dab340`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:9.3`

```console
$ docker pull gcc@sha256:616391d848f730d1153684a657303345189597c73a521db0723d5942c42f9196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:9.3` - linux; amd64

```console
$ docker pull gcc@sha256:043d094a7723cc594215b6accc93cb5f1a217d8afe15047265813a7aebe61ab1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.2 MB (411205415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147dcea158c509870804ccb4c32b7d2268b992f35578203db28837bb4a953cdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:53:04 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 21:17:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:17:57 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:17:58 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b48ca60a82e649783056a8bae6eb8894f16e9775b956a750d51a8a78b5cf3f6`  
		Last Modified: Fri, 08 May 2020 22:54:00 GMT  
		Size: 99.0 MB (98993282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14840e2d1ee496e332c24ce56076a530cb924ba9fb42f35f8c9f0cd30999b4b8`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60089f3984928cfb6171261431dc2199a2ba290bd0b42f4239c934914cce866`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 1.9 KB (1927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3` - linux; arm variant v5

```console
$ docker pull gcc@sha256:4a127d8dcd95fe4bf75f0b96b99c16c21921658451e64e2b6f3303bf20ec71e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369946764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91db00d1d7e215e3f8b89c1fdf2e83f8a7ba7dd31e1be1f94b740128e87b30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:40 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:55:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:55:16 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:55:24 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21447cdb103b079f031307a67f8409e2651baec69f1e51dfd30255356db742d`  
		Last Modified: Thu, 14 May 2020 19:49:56 GMT  
		Size: 84.0 MB (84030481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c8f6d309b6e617dfb4a2dc8008e41b92cf4f12d050955bc33932882de9c9c`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 11.1 KB (11117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf23ae33bdcf5ffdf077b58da736691a306ba623feaa9c4be3993eaed750fa4`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3` - linux; arm variant v7

```console
$ docker pull gcc@sha256:e8467839029bf8145f92b2e123b284187d6a4de9b8ed92fd1bf37e4cb7fcd8fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356703087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803c01f3a15f3ae26e343569892e37fa35953d995da072342efe846699e85a38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:10 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:51:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:51:42 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:51:44 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b26f0ab624e98b8a36880b0e83d19aa9ff313dd5bb0ea2664a4d1e5d8eb2c`  
		Last Modified: Thu, 14 May 2020 19:43:40 GMT  
		Size: 78.6 MB (78592437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82a31e49dd2a244459f157d0afeaf3b5cfd11aea809587fcf12c8583c4d3d69`  
		Last Modified: Thu, 14 May 2020 19:43:07 GMT  
		Size: 11.2 KB (11164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497fc4fbeae3398bee3e76d69dbbc527d55b35f8caceb73dd58859517f4fe19f`  
		Last Modified: Thu, 14 May 2020 19:43:08 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:82b319e3bc433bdc55947c08d514642cb8f61a13a0488275a979e02ef4c6e35a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389278867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25390cfc43d97393ff7fcadcabad238de565470beb9b49f81d16f7a6306bfcfc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:57 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:39:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:39:31 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:39:36 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab669a79249fe8768e08ec233fa7d37c230231da4f6a51f1c564896d14ea3a`  
		Last Modified: Thu, 14 May 2020 19:26:15 GMT  
		Size: 86.5 MB (86522753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad5dd4dfd4c2eeb29f2a2a09a5e46515e5089fbb5c014ce6fda8d69ecfd712`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0292db9e2ccacc650379d717d8cb7b52d111de11c85366c144fd5e6ab83864ef`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3` - linux; ppc64le

```console
$ docker pull gcc@sha256:c706c303b604d83a9b993b175e90d83ef5a37798191a4e64d313cfed4153a187
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.9 MB (431907706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe19dcf35542b3fa03589d13f8d66a11403eaaeb8d33eb01220ef615c737ffe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:27:26 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 20:27:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 20:27:41 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 20:27:47 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a51c27ed7ab734bd4b8836d4989c4e5a045e734cc343dfb22441fca350046`  
		Last Modified: Fri, 08 May 2020 21:40:07 GMT  
		Size: 98.3 MB (98320532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb3ce2c02f01b638a3e9dd6461104e646bc12e2e46f177e8df3fee7e538f13a`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 11.5 KB (11492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c23823132d98a1a06ccc1d9a36b95841809cf92647694dbc240d5587de97840`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3` - linux; s390x

```console
$ docker pull gcc@sha256:ee68155d8a1b2ba81adaa9cd1df17dbc0f9862dfcfda003af488a14ccb64a3a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379468746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9c9379480e41ed171cff59be783300f2a5ff8a7e22af3f774e9d147dd28b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:03 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:46:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:46:40 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:46:41 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee759df493092067547375bcd535956243a61200ff99c1652e15326e07d9b89`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 85.1 MB (85082005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b21a03c089d2af3f5415db551c8845665fad6b9a079343b362d614104430967`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 11.7 KB (11700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2795547afe67b0d409222d9ccecb43cabe8d76f42c57d39efdf8cf28dab340`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:9.3.0`

```console
$ docker pull gcc@sha256:616391d848f730d1153684a657303345189597c73a521db0723d5942c42f9196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:9.3.0` - linux; amd64

```console
$ docker pull gcc@sha256:043d094a7723cc594215b6accc93cb5f1a217d8afe15047265813a7aebe61ab1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.2 MB (411205415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147dcea158c509870804ccb4c32b7d2268b992f35578203db28837bb4a953cdf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:53:04 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 21:17:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 21:17:57 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 21:17:58 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b48ca60a82e649783056a8bae6eb8894f16e9775b956a750d51a8a78b5cf3f6`  
		Last Modified: Fri, 08 May 2020 22:54:00 GMT  
		Size: 99.0 MB (98993282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14840e2d1ee496e332c24ce56076a530cb924ba9fb42f35f8c9f0cd30999b4b8`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 11.5 KB (11534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60089f3984928cfb6171261431dc2199a2ba290bd0b42f4239c934914cce866`  
		Last Modified: Fri, 08 May 2020 22:53:39 GMT  
		Size: 1.9 KB (1927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3.0` - linux; arm variant v5

```console
$ docker pull gcc@sha256:4a127d8dcd95fe4bf75f0b96b99c16c21921658451e64e2b6f3303bf20ec71e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369946764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef91db00d1d7e215e3f8b89c1fdf2e83f8a7ba7dd31e1be1f94b740128e87b30`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:40 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:55:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:55:16 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:55:24 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21447cdb103b079f031307a67f8409e2651baec69f1e51dfd30255356db742d`  
		Last Modified: Thu, 14 May 2020 19:49:56 GMT  
		Size: 84.0 MB (84030481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60c8f6d309b6e617dfb4a2dc8008e41b92cf4f12d050955bc33932882de9c9c`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 11.1 KB (11117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf23ae33bdcf5ffdf077b58da736691a306ba623feaa9c4be3993eaed750fa4`  
		Last Modified: Thu, 14 May 2020 19:49:20 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3.0` - linux; arm variant v7

```console
$ docker pull gcc@sha256:e8467839029bf8145f92b2e123b284187d6a4de9b8ed92fd1bf37e4cb7fcd8fb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356703087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:803c01f3a15f3ae26e343569892e37fa35953d995da072342efe846699e85a38`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 18:02:10 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:51:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:51:42 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:51:44 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1b26f0ab624e98b8a36880b0e83d19aa9ff313dd5bb0ea2664a4d1e5d8eb2c`  
		Last Modified: Thu, 14 May 2020 19:43:40 GMT  
		Size: 78.6 MB (78592437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82a31e49dd2a244459f157d0afeaf3b5cfd11aea809587fcf12c8583c4d3d69`  
		Last Modified: Thu, 14 May 2020 19:43:07 GMT  
		Size: 11.2 KB (11164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497fc4fbeae3398bee3e76d69dbbc527d55b35f8caceb73dd58859517f4fe19f`  
		Last Modified: Thu, 14 May 2020 19:43:08 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3.0` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:82b319e3bc433bdc55947c08d514642cb8f61a13a0488275a979e02ef4c6e35a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 MB (389278867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25390cfc43d97393ff7fcadcabad238de565470beb9b49f81d16f7a6306bfcfc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:57 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:39:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:39:31 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:39:36 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eab669a79249fe8768e08ec233fa7d37c230231da4f6a51f1c564896d14ea3a`  
		Last Modified: Thu, 14 May 2020 19:26:15 GMT  
		Size: 86.5 MB (86522753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1ad5dd4dfd4c2eeb29f2a2a09a5e46515e5089fbb5c014ce6fda8d69ecfd712`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 11.4 KB (11351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0292db9e2ccacc650379d717d8cb7b52d111de11c85366c144fd5e6ab83864ef`  
		Last Modified: Thu, 14 May 2020 19:25:45 GMT  
		Size: 2.0 KB (1955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3.0` - linux; ppc64le

```console
$ docker pull gcc@sha256:c706c303b604d83a9b993b175e90d83ef5a37798191a4e64d313cfed4153a187
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.9 MB (431907706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe19dcf35542b3fa03589d13f8d66a11403eaaeb8d33eb01220ef615c737ffe`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 19:27:26 GMT
ENV GCC_VERSION=9.3.0
# Fri, 08 May 2020 20:27:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 20:27:41 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 20:27:47 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584a51c27ed7ab734bd4b8836d4989c4e5a045e734cc343dfb22441fca350046`  
		Last Modified: Fri, 08 May 2020 21:40:07 GMT  
		Size: 98.3 MB (98320532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb3ce2c02f01b638a3e9dd6461104e646bc12e2e46f177e8df3fee7e538f13a`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 11.5 KB (11492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c23823132d98a1a06ccc1d9a36b95841809cf92647694dbc240d5587de97840`  
		Last Modified: Fri, 08 May 2020 21:39:26 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:9.3.0` - linux; s390x

```console
$ docker pull gcc@sha256:ee68155d8a1b2ba81adaa9cd1df17dbc0f9862dfcfda003af488a14ccb64a3a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379468746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b9c9379480e41ed171cff59be783300f2a5ff8a7e22af3f774e9d147dd28b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:54:03 GMT
ENV GCC_VERSION=9.3.0
# Thu, 14 May 2020 18:46:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:46:40 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:46:41 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee759df493092067547375bcd535956243a61200ff99c1652e15326e07d9b89`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 85.1 MB (85082005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b21a03c089d2af3f5415db551c8845665fad6b9a079343b362d614104430967`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 11.7 KB (11700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2795547afe67b0d409222d9ccecb43cabe8d76f42c57d39efdf8cf28dab340`  
		Last Modified: Thu, 14 May 2020 19:45:10 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gcc:latest`

```console
$ docker pull gcc@sha256:d77a3324ee4cf7313139c92d3f35bcade17214105bf5ee924bc0f284550e811b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gcc:latest` - linux; amd64

```console
$ docker pull gcc@sha256:81f3c9bedf3de5722fbcb3a381ed0e17c6d365d374e0fe863a61c6a6a0780c7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (428977935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bba82d803294cfecf3eeda9e93f2758c9ea0cb15b2e967b229ae91192178a92`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:17 GMT
ADD file:f086177965196842af3c15f50a7f6ad7912aaa7bf73a60b1d00e3129265eec9a in / 
# Thu, 23 Apr 2020 00:20:17 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:50:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:50:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:51:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 25 Apr 2020 02:24:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 25 Apr 2020 02:24:01 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Sat, 25 Apr 2020 02:24:03 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:19:44 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:52:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:52:51 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:52:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:90fe46dd819953eb995f9cc9c326130abe9dd0b3993a998e12c01d0218a0b831`  
		Last Modified: Thu, 23 Apr 2020 00:24:56 GMT  
		Size: 50.4 MB (50382927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a4f197768941ef308d981a94f6d06fb77b9f2ba89dc04d2daf8292ee297315`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 7.8 MB (7812206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc37f14aded2d49bfac62dfa404755c9f1cadfee2b35933e4906f0054782888`  
		Last Modified: Thu, 23 Apr 2020 01:02:49 GMT  
		Size: 10.0 MB (9996197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e27dc593d49a6d728dfe36976cb1469e076fbf3611e501fd030308cd212a80`  
		Last Modified: Thu, 23 Apr 2020 01:03:03 GMT  
		Size: 51.8 MB (51826941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4352dcff781953572c12e05ae2fb6110663338140d5fec17b170e047bcaf4074`  
		Last Modified: Thu, 23 Apr 2020 01:03:40 GMT  
		Size: 192.2 MB (192168842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a33d965e86b92143cd635ebc151cd116eba6ae666c82a4455357f215e342c30`  
		Last Modified: Sat, 25 Apr 2020 06:39:14 GMT  
		Size: 11.6 KB (11559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd8cc6130165afdb489e362815df100adf022784cac64b5bf6d913e8bba4483`  
		Last Modified: Fri, 08 May 2020 22:53:33 GMT  
		Size: 116.8 MB (116765792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1833f92a59cbed26f01e520cccacb1fe0fb9714309fc3ca3882acbca0f9433`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 11.5 KB (11549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80a93c7b003c9fc5379bcc0cf63959b4bc96cbffd53dc57a8e5446242216b07`  
		Last Modified: Fri, 08 May 2020 22:53:10 GMT  
		Size: 1.9 KB (1922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:latest` - linux; arm variant v5

```console
$ docker pull gcc@sha256:67568420cc3b4590ca3c87267130d47657b070bc622dcb571ec205c7dd8dea69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 MB (384043551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231f46631b9df67c6251ec9897c9a19619b70d53361ac1e81d8d833b68f4d78e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:49:42 GMT
ADD file:0d750ede80457d700cc7920bf7758097730f05dd745594645d18f752b03ee4ac in / 
# Wed, 13 May 2020 21:49:44 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:32:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:32:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:36:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:00:50 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:00:56 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:00:57 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:00:58 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:02:03 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:02:08 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:02:11 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:daa20d7c2fc68b19ac519617f67e18594a86dae573165b8260331168fd68440d`  
		Last Modified: Wed, 13 May 2020 21:59:00 GMT  
		Size: 48.1 MB (48105223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1ed27e51f518bb7f9d3d8f217e841fa0e04cec84e4be751525518dcc9a05bf`  
		Last Modified: Wed, 13 May 2020 22:55:11 GMT  
		Size: 7.4 MB (7359297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6799de4bbd5a170a48ae198dc7bf17edd128910c4afe2e792507f17519938`  
		Last Modified: Wed, 13 May 2020 22:55:12 GMT  
		Size: 9.7 MB (9687057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a20c21d3f5a3259a90a0f246387bf2d405adcdbc3d6d94b2d18c8a7cbaa1a21`  
		Last Modified: Wed, 13 May 2020 22:55:40 GMT  
		Size: 49.6 MB (49573343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ef486adcb1a643113e21719dfd2c7c18ad2be283553d146726cb7948530080`  
		Last Modified: Wed, 13 May 2020 22:56:41 GMT  
		Size: 171.2 MB (171166703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ec04f0af4793f44adb8ae38c1af8b08d112d3d83fb95cfcd1d702e1c8a3830`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fb2596fc4b427c0db2a100a6d8710b133dd8fc5d6b4b9aff45eb744126fb55`  
		Last Modified: Thu, 14 May 2020 19:49:12 GMT  
		Size: 98.1 MB (98127258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badfd4878178afb0ea124ffce701ab81db28035fbdc316eee16199b335294ad5`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 11.1 KB (11129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c2b0594177e11ab085897a4cfac99e2c2521eeb90487bdaa9fc6a8588b5a13`  
		Last Modified: Thu, 14 May 2020 19:48:35 GMT  
		Size: 1.9 KB (1937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:latest` - linux; arm variant v7

```console
$ docker pull gcc@sha256:185830f370ea6119e3e171931de533a99ab97b83bb458388087c001efe7425c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.9 MB (368869580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21abb6ce5b250900c0df757d4704ae59cbd1bf27c88dd3337d7fe4270d644ed0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:13:33 GMT
ADD file:8a00a4e8b308e132c6e665ca4e517d4f8b3ba171a2f539903029bc01271087d7 in / 
# Wed, 13 May 2020 21:13:36 GMT
CMD ["bash"]
# Wed, 13 May 2020 23:56:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 23:57:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 23:59:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:11 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:32 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:34 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 18:01:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 18:01:49 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 18:01:52 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:152c1d0ea8a0c219e7a54e8b39fa0bc45d7a9e072c2388cb928448e26aed5418`  
		Last Modified: Wed, 13 May 2020 21:23:12 GMT  
		Size: 45.9 MB (45871321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bff79e1c1f74ad9a60f91709c157c26840bb33b1c4e92d724bad04374160f1`  
		Last Modified: Thu, 14 May 2020 00:20:12 GMT  
		Size: 7.1 MB (7096779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a316208b08652f2aea0cc849622bf6cb91a53f9b10a9d0892580ae96ebb9e90`  
		Last Modified: Thu, 14 May 2020 00:20:13 GMT  
		Size: 9.3 MB (9343194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab435daaee3f8db4fd8c2b79f87c3ae0f33afb42c951ab15d24d8946cf31ec`  
		Last Modified: Thu, 14 May 2020 00:20:36 GMT  
		Size: 47.4 MB (47355396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a0da8a934107507930d13a6a6f22a664fdb89d80cee88a99dec9a59f63504`  
		Last Modified: Thu, 14 May 2020 00:21:30 GMT  
		Size: 168.4 MB (168419252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3c53dc063f5624d9cad81c5683e4bb30dfb53bd30a1b8100ab627c033c3528`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.6 KB (11600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a39cf71475197cb803e8f333c9a4c5aa313a9a761a6a95f5a5889b72ce50eec3`  
		Last Modified: Thu, 14 May 2020 19:42:58 GMT  
		Size: 90.8 MB (90758908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3b1129091b11584ef1685c216e7f790cd9824db10206b4af9bebb57dbeb461`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 11.2 KB (11181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c2f56f8399d1b07c4fb52c8e06d4567a6a16b319a230d806115ba110d211e`  
		Last Modified: Thu, 14 May 2020 19:42:29 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:latest` - linux; arm64 variant v8

```console
$ docker pull gcc@sha256:d44dc0fcf57df5713d3a35f5808e4ed330a5e9addd87759e9993537176d6bc9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.6 MB (411611201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095d30119b6f5c555dc139e92220d731606bce5111170ef39e89d8c60f869a3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:43:08 GMT
ADD file:685903e2621502d2f743969aaf293a5feab58680a95cd93a5ebf2b07f3b5d358 in / 
# Wed, 13 May 2020 21:43:10 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:24:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:24:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:21 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 17:01:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 17:01:08 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 17:01:30 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 17:01:32 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 17:01:36 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:54:26 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:54:36 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:54:39 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:0be831822ade5f87765ba6ff26243b12a3ecd4c379df96483549a7992c1fd35b`  
		Last Modified: Wed, 13 May 2020 21:52:50 GMT  
		Size: 49.2 MB (49168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2879905fcfbdfe9945e6eb39396c6b52b929faf145449ab656f7b35bb6387a`  
		Last Modified: Wed, 13 May 2020 22:39:40 GMT  
		Size: 7.7 MB (7681618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2769f7d2af01c05219ba1529b243249dcedccd56fabeee3d41d792b819f494`  
		Last Modified: Wed, 13 May 2020 22:39:39 GMT  
		Size: 10.0 MB (9983943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e8c22f4290c6000d75544c42d271474d93302f7cd74ef79832ba3c93c962a`  
		Last Modified: Wed, 13 May 2020 22:40:02 GMT  
		Size: 52.2 MB (52155958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9b85452f917a631debce0633df2f9e9a5ee7f79a4d2553949182ffd209a6f5`  
		Last Modified: Wed, 13 May 2020 22:40:54 GMT  
		Size: 183.7 MB (183741566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575aa0a054c8e0ca8e2d081a74c20767c3097bb3e7bcdc6a9b87b976a61c84b4`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1fe54daeaf31c9b21837b776e36801220de4e4caa338fa903a4bb593c10295`  
		Last Modified: Thu, 14 May 2020 19:25:36 GMT  
		Size: 108.9 MB (108855097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ffc610427070ffb0ddfb754cc1685c509ec2039b55edaaaa4e8027b47b1211`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 11.3 KB (11347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94ba3bb67de421a577c388fae447ccf001189416578da6e72432c9177f18915`  
		Last Modified: Thu, 14 May 2020 19:25:04 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:latest` - linux; ppc64le

```console
$ docker pull gcc@sha256:f437cbec3fd8f3330609480bfcd82e22f84fdddf2232c2378ed999dd109ca78d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.1 MB (453132519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3b2aceb0055eadd7e56eb43b15de9a10d42cd37fdcc05e072ad1dbd82a3e0e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:34:50 GMT
ADD file:31369dd617691a0d7181117a065290be8cd8c32814e443ef0a7c7adf7e9d800a in / 
# Thu, 23 Apr 2020 00:34:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:50:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:51:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:58:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 18:16:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 24 Apr 2020 18:16:17 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Fri, 24 Apr 2020 18:16:28 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Fri, 08 May 2020 18:17:29 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Fri, 08 May 2020 18:17:31 GMT
ENV GCC_VERSION=10.1.0
# Fri, 08 May 2020 19:25:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 08 May 2020 19:25:45 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Fri, 08 May 2020 19:26:00 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6bf15800932473d1ca0a2cca9bfac073da118f1172b9027f7e78394850b02d05`  
		Last Modified: Thu, 23 Apr 2020 00:49:32 GMT  
		Size: 54.1 MB (54139621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b057e3462b9249cef48bcf195d058fc780ba16864e4a60f748aef5438a7570`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 8.3 MB (8252627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576b11ea0a4ca8856dec1ec3ce909c13942c2616bd753bc99ee754fa9837da2`  
		Last Modified: Thu, 23 Apr 2020 02:23:54 GMT  
		Size: 10.7 MB (10727087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ce7710ab098018d07af906f197b0de4ecc8a4f1f6f411c31a2f1c00d83b191`  
		Last Modified: Thu, 23 Apr 2020 02:24:33 GMT  
		Size: 57.5 MB (57459761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39890f522a79af437eab5dd9c6644a48c020e9efe096897ec19594b66a2187a3`  
		Last Modified: Thu, 23 Apr 2020 02:25:46 GMT  
		Size: 203.0 MB (202983011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b482b252c1c79218886a279dc727d917bf06ff48fcc2e6880495cb82839e64`  
		Last Modified: Fri, 24 Apr 2020 21:29:38 GMT  
		Size: 11.6 KB (11608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d594e861f679a0e38d19b8fe060dcf02374c4d1774350e40b5b2f042482322`  
		Last Modified: Fri, 08 May 2020 21:39:10 GMT  
		Size: 119.5 MB (119545345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7925dfdd35263e8a915953d765f0919b897526b9f09dbc6d1ef33cb089369`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565b9b6bb59c98fa31c654ce2123bbbb9eec00f2db832cd4fb1e7e6df1ec1c78`  
		Last Modified: Fri, 08 May 2020 21:38:01 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gcc:latest` - linux; s390x

```console
$ docker pull gcc@sha256:2e17a91b3ee6e18fcd83f6e016bd69f8eab8a151f7feba9584d4d2571176924e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.8 MB (394838634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdecee948c99042005977042455fb9b640f3e1ea649ef8a586948f121d81897`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:42:20 GMT
ADD file:8f8ce7623c9f93bb85bf3b2bb1f2515de7b053e11c2efc56feb959322aefc0a0 in / 
# Wed, 13 May 2020 21:42:22 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:39:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:40:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:41:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 16:50:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 14 May 2020 16:50:36 GMT
ENV GPG_KEYS=B215C1633BCA0477615F1B35A5B3A004745C015A 	B3C42148A44E6983B3E4CC0793FA9B1AB75C61B8 	90AA470469D3965A87A5DCB494D03953902C9419 	80F98B2E0DAB6C8281BDF541A7C8C3B2F71EDF1C 	7F74F97C103468EE5D750B583AB00996FC26A641 	33C235A34C46AA3FFB293709A328C3A2C3C45C06
# Thu, 14 May 2020 16:50:40 GMT
RUN set -ex; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_MIRRORS=https://ftpmirror.gnu.org/gcc 		https://mirrors.kernel.org/gnu/gcc 		https://bigsearcher.com/mirrors/gcc/releases 		http://www.netgull.com/gcc/releases 		https://ftpmirror.gnu.org/gcc 		ftp://ftp.gnu.org/gnu/gcc
# Thu, 14 May 2020 16:50:41 GMT
ENV GCC_VERSION=10.1.0
# Thu, 14 May 2020 17:53:48 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		flex 	; 	rm -r /var/lib/apt/lists/*; 		_fetch() { 		local fetch="$1"; shift; 		local file="$1"; shift; 		for mirror in $GCC_MIRRORS; do 			if curl -fL "$mirror/$fetch" -o "$file"; then 				return 0; 			fi; 		done; 		echo >&2 "error: failed to download '$fetch' from several mirrors"; 		return 1; 	}; 		_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz.sig" 'gcc.tar.xz.sig'; 	_fetch "gcc-$GCC_VERSION/gcc-$GCC_VERSION.tar.xz" 'gcc.tar.xz'; 	gpg --batch --verify gcc.tar.xz.sig gcc.tar.xz; 	mkdir -p /usr/src/gcc; 	tar -xf gcc.tar.xz -C /usr/src/gcc --strip-components=1; 	rm gcc.tar.xz*; 		cd /usr/src/gcc; 		./contrib/download_prerequisites; 	{ rm *.tar.* || true; }; 		for f in config.guess config.sub; do 		wget -O "$f" "https://git.savannah.gnu.org/cgit/config.git/plain/$f?id=7d3d27baf8107b630586c962c057e22149653deb"; 		find -mindepth 2 -name "$f" -exec cp -v "$f" '{}' ';'; 	done; 		dir="$(mktemp -d)"; 	cd "$dir"; 		extraConfigureArgs=''; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		armel) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv4t --with-float=soft" 			;; 		armhf) 			extraConfigureArgs="$extraConfigureArgs --with-arch=armv7-a --with-float=hard --with-fpu=vfpv3-d16 --with-mode=thumb" 			;; 				i386) 			osVersionID="$(set -e; . /etc/os-release; echo "$VERSION_ID")"; 			case "$osVersionID" in 				8) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i586" ;; 				*) extraConfigureArgs="$extraConfigureArgs --with-arch-32=i686" ;; 			esac; 			;; 	esac; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	/usr/src/gcc/configure 		--build="$gnuArch" 		--disable-multilib 		--enable-languages=c,c++,fortran,go 		$extraConfigureArgs 	; 	make -j "$(nproc)"; 	make install-strip; 		cd ..; 		rm -rf "$dir" /usr/src/gcc; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 14 May 2020 17:53:55 GMT
RUN set -ex; 	echo '/usr/local/lib64' > /etc/ld.so.conf.d/local-lib64.conf; 	ldconfig -v
# Thu, 14 May 2020 17:53:56 GMT
RUN set -ex; 	dpkg-divert --divert /usr/bin/gcc.orig --rename /usr/bin/gcc; 	dpkg-divert --divert /usr/bin/g++.orig --rename /usr/bin/g++; 	dpkg-divert --divert /usr/bin/gfortran.orig --rename /usr/bin/gfortran; 	update-alternatives --install /usr/bin/cc cc /usr/local/bin/gcc 999
```

-	Layers:
	-	`sha256:6542b1e7bcc740fe79dab47cd5bcdb30fe618acd5d0d0e2583571b2ed256809c`  
		Last Modified: Wed, 13 May 2020 21:46:45 GMT  
		Size: 49.0 MB (48965117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfdd777c0ca04e5c74f52bdae1cc0e2a1ba232e895f109269bf84d8bb598a7a`  
		Last Modified: Wed, 13 May 2020 22:48:24 GMT  
		Size: 7.4 MB (7382349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be4faee9a8c310dbd16b8d77a0a4eee7f207a8cd04340c0852eb46655b9e7e`  
		Last Modified: Wed, 13 May 2020 22:48:29 GMT  
		Size: 9.9 MB (9882141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e46e850fe7f7138b3f6c7d0aa73ac1e5c4d1c8ee2d6272e32c6727088efcd9`  
		Last Modified: Wed, 13 May 2020 22:48:43 GMT  
		Size: 51.4 MB (51369321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f78e7e65e237be1d924b8cc10d6a39902a63883ea34c4836d92c32c45007c62`  
		Last Modified: Wed, 13 May 2020 22:49:11 GMT  
		Size: 176.8 MB (176762581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486847615c30af89f0eca9a07fbc419bc2c2df8c49d7bacb42ea7ead4a2f7e95`  
		Last Modified: Thu, 14 May 2020 19:44:14 GMT  
		Size: 11.6 KB (11604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df604c60fd52716f44861b5c9cd7e7170413a449dbf7a2ca434d2f112ed1a3a3`  
		Last Modified: Thu, 14 May 2020 19:44:30 GMT  
		Size: 100.5 MB (100451895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000b3e8df7d91b0e25950beb75592431163c7fcd629953ebf853dccf0f7eb2e`  
		Last Modified: Thu, 14 May 2020 19:44:28 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5ae588af340eb12f25c24bead1d2981fb2b2d30b64f187bf2aba679b072a8c`  
		Last Modified: Thu, 14 May 2020 19:44:29 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
