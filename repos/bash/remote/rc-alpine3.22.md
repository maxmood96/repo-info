## `bash:rc-alpine3.22`

```console
$ docker pull bash@sha256:081b6b5916b935e419904a2aec09e04e5e5c82415cff2e68e18eec2c7c01c4c3
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

### `bash:rc-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:211322bf62efd027170186c0c7a206d4bd639a4233e1e942ac805b13dd2c1f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6756507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb720d9cce4663991c8cd1e97192786cf8a037ae19df335a2ccc6a90d583523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eb862a7e6e5e380a0223887b3e15875cbac9c578436a351ee7548b70a6ab18`  
		Last Modified: Fri, 30 May 2025 20:49:11 GMT  
		Size: 3.0 MB (2959331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e898da1d34fd396cb15698b847573dace9267f8392ac240c2777d3454b0bdf`  
		Last Modified: Fri, 30 May 2025 20:49:11 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:b182ccdbb67c8e7dd024996daf510bac6e3e0d1ceb7c2895f5d2374e1c7ba2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 KB (139354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303a6a2f5cbe61ae772e0bf7a24b939289f484ffb2ae687dc5a310f5e12a7d63`

```dockerfile
```

-	Layers:
	-	`sha256:520f869a7bc48241fb6e907b8e329de135570cae20f8ffb87e964abc17c54c7d`  
		Last Modified: Fri, 30 May 2025 20:49:11 GMT  
		Size: 119.0 KB (118999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef6bc79b49fc01fa54f99355a30e9f8f151a1e298bc2245a04b466ebef1b8dbc`  
		Last Modified: Fri, 30 May 2025 20:49:11 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:413a25df5a3627b1fe2a886a8d80d3b4f7fdf5e0c3a2f88ba8b8759b4c96f19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6397646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4be29a36e566551c2cde76a1c06c4c12230b0c33896a65b28bcb61c5842d970`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Fri, 30 May 2025 18:04:31 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d9c2b773e1c0803c7e83a46a0060cafff883d8787f3d0229ab4a14d4648dcc`  
		Last Modified: Fri, 30 May 2025 20:50:18 GMT  
		Size: 2.9 MB (2896379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d708c4ce0fbe8979e1eb1729e7cf693fd4e88d162bf6114855df40bfeddcdc`  
		Last Modified: Fri, 30 May 2025 20:50:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:910ed23c28e0eb257eea6abfe726a05c6da2f28510546b3937a2841b8fd5ad1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8405210b5e08c52397ad104a8d5ac42b2a512607e94bf9d549da7dae93066114`

```dockerfile
```

-	Layers:
	-	`sha256:afb9e758e0f229709d4005f466ce0e264e4810fc17296e7dc9a727337a669264`  
		Last Modified: Fri, 30 May 2025 20:50:17 GMT  
		Size: 20.2 KB (20232 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:25187cd3297996e4fdf5f241026027bcb4106e03c0967de8531b30552d7c61a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6066700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6d2466190b78208e875a52271af3876939379350902e8eb08f618e7827a44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Fri, 30 May 2025 18:14:23 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de81f0d7214f7c1eb70e7b1477a19fee686e4179609fea6cd93d7cfe3fb86e4f`  
		Last Modified: Fri, 30 May 2025 20:52:10 GMT  
		Size: 2.8 MB (2847187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c84e7d44df6a716db93037fba5b3f7605640b85df1c752553e918393ca24d48`  
		Last Modified: Fri, 30 May 2025 20:52:10 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:6eb37ccf860e6a059027b76fb001e033ffc219be54141a0f6769ae40c931a3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 KB (139498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2803b052e3a2cd33baec5cb0fb5e75d4f5509608a12f656eea42ede8dae2a35d`

```dockerfile
```

-	Layers:
	-	`sha256:e4c66996bc29001837f688d2431eb184fa42e7f79283aacd3c3c7d2604669a61`  
		Last Modified: Fri, 30 May 2025 20:52:10 GMT  
		Size: 119.1 KB (119051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17c364b7ad7962030a4e96f841b99ec579c92452a1b92ba93053b998e6b7875`  
		Last Modified: Fri, 30 May 2025 20:52:10 GMT  
		Size: 20.4 KB (20447 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:81cd11be184e5227ed6c521aeab574614c6bf5beafb02c090ef29292f5774f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7183391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78abef7d2ec1cb1a9f4a9818a30dc2b93ada69ecb77188f8035f72d47ddef6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Fri, 30 May 2025 18:15:21 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b20e202572e93ca6e6d210bf4479c5a2a4d2422e9d6987c4c500625b3e53f98`  
		Last Modified: Fri, 30 May 2025 20:50:22 GMT  
		Size: 3.0 MB (3047114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7925d4038828a967c0a323009d608b8961ef9dd8214dee780d686ee31880e005`  
		Last Modified: Fri, 30 May 2025 20:50:22 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:4309b7e7edc3c92eca46e420b4431a86b487be164d414fa80d329f9d626dc550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 KB (139562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b116249a4b1a0f9045d3c8cc98e1e3aaa94c9e205aca44e0d416b6019a4566f`

```dockerfile
```

-	Layers:
	-	`sha256:1e5a82cd3e5dd4150b287f36b37e1d90f5120ae554531f3ec36e8f4b8c2693c9`  
		Last Modified: Fri, 30 May 2025 20:50:22 GMT  
		Size: 119.1 KB (119079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93812e333f07f2f6a8701e904d53764a62869bdd9fb506641ca85025d381e67c`  
		Last Modified: Fri, 30 May 2025 20:50:22 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:0378c3fc732059fd827090595da91ac1005ee192a1ba78cc967b6eb35dd29bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6502472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8338cf6f0d71736b01b880c011e2cb5f85b667a1cd54c8706409ed49c91d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea44bcef65ee1d93b568e97774d561528e8bbcce96ccc910e6b9670f8b41ca6b`  
		Last Modified: Fri, 30 May 2025 20:49:15 GMT  
		Size: 2.9 MB (2886104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d00b4d78b8903ab37bad1c3badab294bee381adcb39407a832ebeb85515e6c7`  
		Last Modified: Fri, 30 May 2025 20:49:14 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:db572179be709e6ce95083b125c769f6e766670d6f8e06ec715c9069af0352ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 KB (139277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7477d861b78278368cb0d00bf2fd49afa43cf4f3e523db7383460f788da9c706`

```dockerfile
```

-	Layers:
	-	`sha256:f20d1459fb1bc4bf3273600fc6fbadac05e5e9b027d140b909ae8655a98f0d2d`  
		Last Modified: Fri, 30 May 2025 20:49:15 GMT  
		Size: 119.0 KB (118964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c7bdeaf12bf7422df29fcf55caccd675d3d89d94d0504cd95633d780683a03`  
		Last Modified: Fri, 30 May 2025 20:49:15 GMT  
		Size: 20.3 KB (20313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:6f8d489b43cb4f5d06f8af3b9e734913f9ac4caf01da4cc566a18f2f0f69516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6962471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79f6d1a52aff9cf112ca85a2874f3d9392c17f03be2f05e75e99180e00d175f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Fri, 30 May 2025 18:14:22 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a00071bcdc22558bd11e4f93dd086d0624f00e2a770d11fca5c354493e0edd4`  
		Last Modified: Fri, 30 May 2025 20:50:34 GMT  
		Size: 3.2 MB (3231948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9de8beecd71d937488ce6952f7069223b735a3e5bfd9c70c3b187f453642be`  
		Last Modified: Fri, 30 May 2025 20:50:34 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:d7a8d7abc860cea24b11999e195c4742d79f07e6452ade21fca2081135fcfe00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 KB (137505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda0aed6d8b9b3199f5bb3a0b5138e40f32a41b3e35d2644f8d5ea20c04b2d58`

```dockerfile
```

-	Layers:
	-	`sha256:90d601142943608bd0a1ddf9c2af392bcddf98d2c88d3be769647ac1db9acf20`  
		Last Modified: Fri, 30 May 2025 20:50:34 GMT  
		Size: 117.1 KB (117094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ed11163f5ffa57d360ec6a8948c40e1ead0c64b7e62d4e97a127e845b2f836`  
		Last Modified: Fri, 30 May 2025 20:50:34 GMT  
		Size: 20.4 KB (20411 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:7827723176117a635a0a9ecf17c1ab36fbb750ce3e0fbc23e7dd376d978248de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6423757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d10498a306c52d8e4e09ed1881878cab52634cbdfd4a9d104954fa55abdab5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Fri, 30 May 2025 18:54:40 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0395a1c8ce5a6ea62c64f32f34fb05281cf28e2a63fd5bae46b813b38dbf5f53`  
		Last Modified: Fri, 30 May 2025 21:08:00 GMT  
		Size: 2.9 MB (2909610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3196eb45a940a237c7e685d0bbd88f7143c3039eecbe9f1a0c1a49105100467d`  
		Last Modified: Fri, 30 May 2025 21:07:59 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:eedfbd40f53f5dd140ab8bf79308fca67df21cca63b8fd578b5132532401b24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 KB (137501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785da4fb6876276d9d5e659dccc1b42d6471538421a8100800c8b742075a30a1`

```dockerfile
```

-	Layers:
	-	`sha256:7780ee62ed9f8b03e818348dfd1940636a5b747c7538cb67a03f5c4d0b42d332`  
		Last Modified: Fri, 30 May 2025 21:07:59 GMT  
		Size: 117.1 KB (117090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d216898cf344ca34775a74cdc879ea95be5e0fdcb4d1c0199d3ec246b5439d6`  
		Last Modified: Fri, 30 May 2025 21:07:59 GMT  
		Size: 20.4 KB (20411 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:f3b58a8767dcb5edce6f30d6db5677961f4afd65473423829f929f842e6d7639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6704559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f94bdd5129df4837e3bc4a7fdacad5209deffc72927e91725acb53542aab236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_VERSION=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
ENV _BASH_BASELINE=5.3-rc1
# Fri, 30 May 2025 18:52:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Fri, 30 May 2025 18:52:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 30 May 2025 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 30 May 2025 18:52:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Fri, 30 May 2025 18:13:14 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb506e74a4dd280ed48dd2bfacb876fd330a795b0a1d787c69352ee4832051d`  
		Last Modified: Fri, 30 May 2025 20:50:45 GMT  
		Size: 3.1 MB (3056693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5aed3882a8f7a3655a5d19de5e661f65a40cc0201b5c4d92cf6aafd94458e3`  
		Last Modified: Fri, 30 May 2025 20:50:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:3ff0b75338b41ed59ce6c6345f0ca07fc4cc2444a903f27f684a350e70df40b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 KB (137403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cdf7283d652c74a471d44dec29f72d5a18bebd189bdf92ffd7b8f038eac1cb`

```dockerfile
```

-	Layers:
	-	`sha256:fd02c7def18bda0c5d3e7faa7e3ff0f86eeda6733ed4c8a145ee5d326e807a31`  
		Last Modified: Fri, 30 May 2025 20:50:45 GMT  
		Size: 117.0 KB (117048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf7c6b469ab7e5a4edd79f82764bd3de1079a4858d0ed84343d34ed3db2df84`  
		Last Modified: Fri, 30 May 2025 20:50:45 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json
