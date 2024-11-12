## `bash:alpine3.20`

```console
$ docker pull bash@sha256:4bbfbe07eceeed5ab9136b37faf4f5cff3c28a339087ce068a76f2c1733054e8
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

### `bash:alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:69d156705ff4829e60cd958dd356e8db024195efcdb0504eb3426c84647c6e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8232586933a198a72bc7bac46632290a504aae7c97dfb3c6a092220ae0070f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04a532fe6b3090c443d3b77bfd0eac9df544aae821dd8042656b3ae67c0f1e4`  
		Last Modified: Tue, 12 Nov 2024 02:02:07 GMT  
		Size: 2.7 MB (2694573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4b3a33902803938e5d80451e77d2dad62576c6bfe2b6b0c00ef50ad56878ac`  
		Last Modified: Tue, 12 Nov 2024 02:02:07 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:b493a95f91ae8c377738fde8352eaa8e9ece51490bcf221ca677a5ad40d9f4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 KB (132277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210fa39028a129347a4659e2845f85622e9169546cbc548c14722b28da42de7b`

```dockerfile
```

-	Layers:
	-	`sha256:2d407759201aadbee4417f2303f78986ad6d9e1239795ec084b7e5fb5c5b5a62`  
		Last Modified: Tue, 12 Nov 2024 02:02:07 GMT  
		Size: 111.2 KB (111243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39475023a60cff8a95f4afc4c246907c8d9d08ed33f99b9ebcd163a83afc805`  
		Last Modified: Tue, 12 Nov 2024 02:02:07 GMT  
		Size: 21.0 KB (21034 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:481160c538a39b9b7d7860ccfa43a0003bd8e9b7da3992b8856b8b84adc167ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee99e8c3541ff0558243b0dc05f06c3ff704d0319426501b053a7f3e09e6329`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852bb93381af1da13451e26483c6db7f93d212e162efe8e49a9b2d4081005d43`  
		Last Modified: Tue, 12 Nov 2024 02:03:42 GMT  
		Size: 2.6 MB (2637625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc63a43986eab4919a11e9263054bd8f1cd476bf8a84462aa45c84fa23dc80e3`  
		Last Modified: Tue, 12 Nov 2024 02:03:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:b7f104950f806e7ca5cd34992a239185ebc8c712a4651d88608b33df08a6e1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 KB (20927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300b7c09868d570e19e0865725b98661b697e06efcee0b785225c6ab16310aad`

```dockerfile
```

-	Layers:
	-	`sha256:f487a804531db1fc08260a70060befc7cb53373492978bb2bd1deac11c4b2570`  
		Last Modified: Tue, 12 Nov 2024 02:03:42 GMT  
		Size: 20.9 KB (20927 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:44dc0cc80884d7dde174b3b11faea2326f4f2cd21ae8934d381e3fc57c3864ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5686834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd3a09644332ee4257608d02335f7a3f96ee8aa377e663d4fed9b742e32cb74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ed7c85e37297f03e774380d6b0cbcb5e33b0004cb3b8b1a211fb254c17c964`  
		Last Modified: Tue, 12 Nov 2024 02:03:37 GMT  
		Size: 2.6 MB (2591017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167950dfb9f5d5019bc60f0aadc8c572a155dff2993e7846a5e75d88a6e76271`  
		Last Modified: Tue, 12 Nov 2024 02:03:37 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:cd89526bbcfa8e8285e1ab654d5bd065ecffa6cfa1251cc5c8ca71cb8a702841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fa168227bef812fd7d7cb53caf9f34bd427fe3f5c23390c70789f9496e3d41`

```dockerfile
```

-	Layers:
	-	`sha256:e0d5b5f8ae4ba3225b8ef8563d9d0189743f6c10e275d8be3ae52f05813998b5`  
		Last Modified: Tue, 12 Nov 2024 02:03:37 GMT  
		Size: 111.3 KB (111311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6251cd33eb2d10f6607a95600616f0f041522c2ac48cd306494afff44b26e3dd`  
		Last Modified: Tue, 12 Nov 2024 02:03:36 GMT  
		Size: 21.1 KB (21141 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:be10b22101db3f640c3ff3400b8bded1404cbd94d55bf92f2e9efa16ba31d0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6869256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fa05ef586657c6d9932c02ed0a5b8f0348ba8dd930062da46fd262f0cc432f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0d8fc08357ee7a33931cea76d5b05be4f12458110dfaac28952664c45b11b4`  
		Last Modified: Tue, 12 Nov 2024 02:07:01 GMT  
		Size: 2.8 MB (2781201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9841dbefbce990ee46e8f435805ff33fd1224ef4a05570d4c5c561e176775dab`  
		Last Modified: Tue, 12 Nov 2024 02:07:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f707d6fd4643d2b80ad44c0199fe647849b2fd13e5260f438c8a345ac8d42f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80937a2f297800a06a046c270709abd30fb05a4742378013ef82581e2d298693`

```dockerfile
```

-	Layers:
	-	`sha256:c4fca1b3282d7b25b1d6ad68861601c45e87b56037e729759a3c2cd7d7a6bfcc`  
		Last Modified: Tue, 12 Nov 2024 02:07:00 GMT  
		Size: 111.3 KB (111347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a781ffed8167a544413a5a1d5f487c2125b7efdd83427fc0a57fe82922859f1`  
		Last Modified: Tue, 12 Nov 2024 02:07:00 GMT  
		Size: 21.2 KB (21186 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:d94457affd5f72d97a28e772e18cf6d567abcf5529944ef89dcd52a960b7e373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6113954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abac067fe999360c426f426f7e8cd13b23e320946895b4e49a81ca8a4454f51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bd2e360c1f587f408e442b9f4f47da2fc4a2c1bab3d2c504ddfcf1e2a28d7`  
		Last Modified: Tue, 12 Nov 2024 02:02:10 GMT  
		Size: 2.6 MB (2644402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db307df2deb0cff5cc9f5c1aa4d0fd00b3a25d2104676181d187428f1d85ef0`  
		Last Modified: Tue, 12 Nov 2024 02:02:10 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8b4766a655aa3d5ef746bc512e26b0e709fbea9e2619390c7de6dff9774de340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 KB (132180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fdd19ccb709edcaa62f8a70e4a86e218cc371a10015ffba14a5bc40c2df26a`

```dockerfile
```

-	Layers:
	-	`sha256:99913be589407c067091a3c89d370603462fc4e0b24e1f96cc114d64ac00a62b`  
		Last Modified: Tue, 12 Nov 2024 02:02:10 GMT  
		Size: 111.2 KB (111198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fae0d8e3fbf99ee3dbd56bc2e96480e04e78df4cfd9be2d454e7f4c9bf12eda`  
		Last Modified: Tue, 12 Nov 2024 02:02:10 GMT  
		Size: 21.0 KB (20982 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:cc2e93c4ad36cc90bdc2eba5acc184ed878dcb49ad480cd94f9e308b98ce6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3e1db5d21d1794e7d731499ab96631a425e001755db22e27b25f4755801fda`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5889c29eb22a9e78370dfc171bb88abee3bbd800eaa619c02c593cb170633e30`  
		Last Modified: Tue, 12 Nov 2024 02:04:16 GMT  
		Size: 2.9 MB (2945358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adc4918554be51afa7c1cf0c7c9150244779dd29f024af6d1fcca9176c72df9`  
		Last Modified: Tue, 12 Nov 2024 02:04:15 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:41afe5ea50664a7ac3a53faa8fdd189ef9797d16e08dd3e4269b14db54895559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 KB (130449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ee95e60daa0ed33b77f540877f791d922236f642f305c77c718311a961066f`

```dockerfile
```

-	Layers:
	-	`sha256:7e941d1679540a1cfdcd88b47cc10f0feb484ed04be56bf933adf06c8b6c82d7`  
		Last Modified: Tue, 12 Nov 2024 02:04:16 GMT  
		Size: 109.3 KB (109347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b03aeefdd392d6d7f8d93fdc860cf3e5d8f896e2b21f42a638119d0ed3fca59`  
		Last Modified: Tue, 12 Nov 2024 02:04:15 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:2988c6807b874d79ebe2dddfbdae327b412468078997a60fb16a2c4bba8bce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6027430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a76be1bedf49701f460bed8691d15c4a19bcd68244a7e5705fcb9dcba048d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df74a3ccf1d88ed3d1cb39e0676bb61330efa5ff80636d28d7d694b42bc01bc4`  
		Last Modified: Tue, 12 Nov 2024 02:24:56 GMT  
		Size: 2.7 MB (2655610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236acea71b6323db9ef7703fe7efb77b736c7dade173aec93a31cb800e8fca0d`  
		Last Modified: Tue, 12 Nov 2024 02:24:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:11195bff065af2d75991add4b57835e91951086bf4c4b8d5cb22b143fb20e3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 KB (130445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ec3c26c39a33b198f8e26ce2e22ec1039c8b1a88c9f9f775d57455bfc0a502`

```dockerfile
```

-	Layers:
	-	`sha256:2de49dcdcba4ee3c28f1ddbf579ed2a6e948c12140d76c5a4a1c5fbe9fef79b2`  
		Last Modified: Tue, 12 Nov 2024 02:24:55 GMT  
		Size: 109.3 KB (109343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15d72daf9eb5e7367f742e55ae5c228da511bdbb960e8012d63aabe6bc35a89`  
		Last Modified: Tue, 12 Nov 2024 02:24:55 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:e6cfe72e738a8b89e2878d368eb77807f309deb000b5b2713f3499fa6971dd7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0345f9ae22ef7fdd8964276220071aec07db939d723244c64bcc207406198`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_VERSION=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE=5.2.37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_BASELINE_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
ENV _BASH_LATEST_PATCH=37
# Mon, 23 Sep 2024 22:17:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Sep 2024 22:17:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Sep 2024 22:17:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f486a2c07a72ebdaeff2381748241e55d5566607f07b41c77054f56ea4e602`  
		Last Modified: Tue, 12 Nov 2024 02:04:13 GMT  
		Size: 2.8 MB (2782317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169b4775da9e5090c594bc8ff9199591144e90a137abcd0f26e18f28b678b146`  
		Last Modified: Tue, 12 Nov 2024 02:04:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:eae11e367f4809b70dbcacf5b6b2c662380ea123bef7ae0ea446a7e93a1952ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.3 KB (130323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e055b1a011fe27f571aa14efe09b10f2113c7b8dda2025629bf0866b0e416b`

```dockerfile
```

-	Layers:
	-	`sha256:efc478473a39d9a1934f0a722cdaadab15ada415b71cbf9055c3d93235d127ee`  
		Last Modified: Tue, 12 Nov 2024 02:04:13 GMT  
		Size: 109.3 KB (109289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea85da776f38caf05b023c5863ab9330f3fdeafd2feae12d772baa50389d726e`  
		Last Modified: Tue, 12 Nov 2024 02:04:13 GMT  
		Size: 21.0 KB (21034 bytes)  
		MIME: application/vnd.in-toto+json
