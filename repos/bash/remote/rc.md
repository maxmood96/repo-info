## `bash:rc`

```console
$ docker pull bash@sha256:b39c9fcee2686e4be9b3e777c3abb2a90e6490a6bc6267113e881b50483423ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:rc` - linux; amd64

```console
$ docker pull bash@sha256:9d7d6e5cbca25f603350c58b9854054b286c372549a85cce6cf7bbed9017be9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6510251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea44f0433f10d41669acfb9679dad835db7b1dfda52bcf165ede88829bf2fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3976cf0e4c03a72088cece1f942ea886dc0c104a744b474fb5a8891317793bf8`  
		Last Modified: Fri, 06 Sep 2024 23:15:47 GMT  
		Size: 2.9 MB (2886110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd247a0f541bbfb923380076e766a7bc5bcb40144ab66c95cf0c9920427b3a65`  
		Last Modified: Fri, 06 Sep 2024 23:15:47 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:e09e9b4b3a5d1413deb46397ffb7848bdd4beec26a5a9c3e96a202c585f48750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 KB (130523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cd08cd22ebe784e58974f0d79209a7be6fe16f76f985f3e06fc6acdd8a1255`

```dockerfile
```

-	Layers:
	-	`sha256:892633c8c1be2cf5afa1de6788522d35c8edc5e76b8790ffd11ea401ecb50f70`  
		Last Modified: Fri, 06 Sep 2024 23:15:47 GMT  
		Size: 110.5 KB (110461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8949fb93521ad6ead433ed2c4dbb314fa96866a82776718fb89c13cc061cea`  
		Last Modified: Fri, 06 Sep 2024 23:15:46 GMT  
		Size: 20.1 KB (20062 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm variant v6

```console
$ docker pull bash@sha256:98b2a038ccf335f705b90790ec281761f04107747548aae5ad8a1629b882ef94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f72d3a73aac246faa1ac5efb6793c2dbcf54dd7cac9aed5254e9b841edd963`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a124718ee25caf0931842fa1fc9017fcee271a5198ce8c0869b8c5d984e7b43`  
		Last Modified: Sat, 07 Sep 2024 00:58:28 GMT  
		Size: 2.8 MB (2837467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef442d6b113272fadc1acee4ead41815bcc5d5dd640e2dd6ace06bb2f04fba36`  
		Last Modified: Sat, 07 Sep 2024 00:58:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:80d501dd2444f95a925f35af017dc1f928c31a4e800c183b7dbf6ad8de3a4842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9584351ed2277c8039592d3697e87b8436e1ebf82fac6c0f081c0d88029edd29`

```dockerfile
```

-	Layers:
	-	`sha256:3d9a635fa39f0579426e0cfa3a1422e8835cc85174f8017c20db32ca7cede4d3`  
		Last Modified: Sat, 07 Sep 2024 00:58:27 GMT  
		Size: 19.9 KB (19929 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm variant v7

```console
$ docker pull bash@sha256:9cf93846e0dd562a23eea2e596bc98bfe50f38d9c3c73792cb1f68b3e8cc01f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ca4d05dff37f98bcac815cef97b626f74643a533d7e2b57cc4cac9e27e1da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215aeb726716254ba24ef9b3e4b3894018d57b76bd1e30ce0ca8ceda22bca42`  
		Last Modified: Sat, 07 Sep 2024 00:09:14 GMT  
		Size: 2.8 MB (2783086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c26cb487f42fc8907a05f86c53c9df2d7bf53b54d4d2ab9254cfd85097dd73`  
		Last Modified: Sat, 07 Sep 2024 00:09:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:89baaf2765d5f917c80c1e1fbfd4eecbd3f7c29231a99b4b54703bcf01f1c53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4237d6013cc3252ba7142270bf6bc138dafdce3eabb09ddfdc3c15706438c8fc`

```dockerfile
```

-	Layers:
	-	`sha256:51ef5b2fc890eaea378fdbc3a2783aa70e976f73d1933e2991bf6ab115bfa623`  
		Last Modified: Sat, 07 Sep 2024 00:09:14 GMT  
		Size: 110.5 KB (110513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602f40eb099e1096635a162dce87dce0e14eea5acdc4fdac8626f9a675f724d4`  
		Last Modified: Sat, 07 Sep 2024 00:09:14 GMT  
		Size: 20.1 KB (20148 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:2fd479cbe70504fb1f58adfd14618f9f20d14388a63fcde8d411f1b7750b80e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7074873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c90c18c904df2f49b89c55d1b379bb762639ddb8e9b36cd6c0bc0a662e92df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae61f31cabde658e54e79b3be2941b96249c8a4ce671e3b11ffdf462bd8a0a7`  
		Last Modified: Tue, 23 Jul 2024 11:16:35 GMT  
		Size: 3.0 MB (2987603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0e9e4945f1e08004c1441193317d4fb111b011e23f6af349d512aeffdeebd6`  
		Last Modified: Tue, 23 Jul 2024 11:16:34 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:b6b9ddb077fda20d74959892d612f84a9357e3eb11295f95c95b8e3685b921e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8d8a2212f4fc45c50a41af22a4c5976e81ca812d094176d44f49ba40871149`

```dockerfile
```

-	Layers:
	-	`sha256:e811198c18a25d034c85cc143be385d1878205795d98137f55b8f1bc25dea223`  
		Last Modified: Tue, 23 Jul 2024 11:16:35 GMT  
		Size: 110.5 KB (110541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae72ae1a50cafc37535d4f7cc89b62be1388c016cfa2cd5f650cc408ac5494c`  
		Last Modified: Tue, 23 Jul 2024 11:16:34 GMT  
		Size: 20.4 KB (20386 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; 386

```console
$ docker pull bash@sha256:0bb74f9f15ef168a885731f3d7624666b086d061f0bf5a6e041a253bf4d7c631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578dd85724c64d80d69ba46f0c694c90ba56dbbb4fc04eb9f448e4c43ae32bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d691c82d5b4d37b753bbdb26d5644ed1539cde1ff1e3157c8edc97dc4892de3`  
		Last Modified: Fri, 06 Sep 2024 23:15:53 GMT  
		Size: 2.8 MB (2826650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafc2ef18502e850fc031c255a7840fd8fa9dc765f78f4316299e44c773ed704`  
		Last Modified: Fri, 06 Sep 2024 23:15:52 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:7747f57b31c24cf01e234c16baffb41bd8787ded090d38c452d7777587dea01a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 KB (130449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1858ca0e925efdf7a2854388ad1243a45f76734da5b3d221824f7e3b372457c`

```dockerfile
```

-	Layers:
	-	`sha256:155400aec506829ba0f2a1306cc7542f05bcb860ff703a3b5e2d492225410a0d`  
		Last Modified: Fri, 06 Sep 2024 23:15:52 GMT  
		Size: 110.4 KB (110426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e446f4520cdec6a20598e4c28c58c07b840829535f0a0ab8d87b2c52b2c0d6f6`  
		Last Modified: Fri, 06 Sep 2024 23:15:52 GMT  
		Size: 20.0 KB (20023 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; ppc64le

```console
$ docker pull bash@sha256:c92dcfc85c4225d74a8b2baaaca3538a2700b224b73d513c1978ff38f92b2a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6729533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac5dc3539a9887c05c662d1e640f36ae951313c2614dcf80873bec14781d39c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceabe5c50379b93dbb5255d31e69895e31741468e8189c05f13b0472437703bc`  
		Last Modified: Sat, 07 Sep 2024 02:14:08 GMT  
		Size: 3.2 MB (3156777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1ee8fba166bf66c37cabf1bd3fdb69e8d72444d3c15d7ff8faf09cc0b98981`  
		Last Modified: Sat, 07 Sep 2024 02:14:08 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:33f7984f5e804d992def1c54b1eacdd1e238c8cd0950260310219dd093f68896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 KB (128665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1eef3bcc0e626a18b0d7ca9375b1fef4a12113fee52dfb61ab29e85a5703b7`

```dockerfile
```

-	Layers:
	-	`sha256:90c42d15e41065ba38ebe73514cc249d9cacad745e43082ceec1a47e7be2ebc6`  
		Last Modified: Sat, 07 Sep 2024 02:14:08 GMT  
		Size: 108.6 KB (108553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2431ac020d89c662d0c0f0d266d6ea5a21c5586f436b8dc05bbd30d04fe160e3`  
		Last Modified: Sat, 07 Sep 2024 02:14:08 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; riscv64

```console
$ docker pull bash@sha256:08e5e7aae8d6a6edc34eb9a50879ae2249719a5858c31149d903bb78560c7382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568d2837bd12a9e4583b2b8f5ca0816639b4e123c81e7e5f7173c930fec1d6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a766849be4d8ff607224c58b5e4d144219b779f312c30119563b67b4f31eb58`  
		Last Modified: Tue, 23 Jul 2024 16:58:45 GMT  
		Size: 2.8 MB (2838922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2166227fc1fc79b4d0b8c0a2748d8cd16d393a4e236b0380c7390da677d198fb`  
		Last Modified: Tue, 23 Jul 2024 16:58:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:c0bd9a70925bdac8624395c4862fcde10e097288d521fa351a98a99d821a1eba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 KB (128661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a826ced5d35d2748d5fcd687248fa257a36bfd6549b75dd628015769ba0fb68c`

```dockerfile
```

-	Layers:
	-	`sha256:fa09436e17c26d79ab7c412f9008e8608b6a9d8512defce5101091782f6d6160`  
		Last Modified: Tue, 23 Jul 2024 16:58:44 GMT  
		Size: 108.5 KB (108549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a407d8cfb1796471923a5fb5f2b7fcba8b2e160ec39d7d50be615282a9136c`  
		Last Modified: Tue, 23 Jul 2024 16:58:44 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc` - linux; s390x

```console
$ docker pull bash@sha256:8854bb5eff05a533e673f66407958561fb53c474035ada76909c5b550194b676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6448966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5358d2ce580b10fcdd5dacd1b54f14fa34ce54063f912e55056d56851b5c854`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Wed, 22 May 2024 19:31:20 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_VERSION=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
ENV _BASH_BASELINE=5.3-alpha
# Wed, 22 May 2024 19:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Wed, 22 May 2024 19:31:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 May 2024 19:31:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 May 2024 19:31:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102cfc7dbcd080a3b76e46403d3a364d0bafa8eee1abcfb93dd3d8270ec5ee4e`  
		Last Modified: Sat, 07 Sep 2024 01:48:25 GMT  
		Size: 3.0 MB (2987031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5253cec7bee7a139a8cfc3d2181268825972f24a06de5fe8368ec78ff0015ca1`  
		Last Modified: Sat, 07 Sep 2024 01:48:25 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc` - unknown; unknown

```console
$ docker pull bash@sha256:7bac6aae1850ddf057a734e6b577e52dd226e1e5613697f50a51c15fd56b858d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 KB (128569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2d4f4187c78f78cfaa57329c58d3cf0772449e5ea2ddd1d03b37fa6b73c187`

```dockerfile
```

-	Layers:
	-	`sha256:c97f7ce26f49ee0e109d678f874a651bc3f51a6b2b0786b060e7cb8564ce2d11`  
		Last Modified: Sat, 07 Sep 2024 01:48:25 GMT  
		Size: 108.5 KB (108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2574d696d2c6f23496533fc867daa5808b2ac1c75481d95f7c37044e8da203ba`  
		Last Modified: Sat, 07 Sep 2024 01:48:25 GMT  
		Size: 20.1 KB (20062 bytes)  
		MIME: application/vnd.in-toto+json
