## `bash:rc-alpine3.21`

```console
$ docker pull bash@sha256:05c56a4600ca2fabe36e434e13f9a8e40b252b086e507ed0cf07adef765f8c67
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

### `bash:rc-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:4a31981374fef45e74a49ba53474d662a8e6d033fb39d8b074ae8a66fcd12a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f3757d288d016e589a44d84cb3ac52a1901649b9b6e75a49aac6c1343ffd94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e218625d7849dcef74a034e7f7b3bff456d25afa77f7bf25fe182f443c374`  
		Last Modified: Thu, 08 May 2025 17:48:38 GMT  
		Size: 3.0 MB (2958722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2501ba568cc690b2670213206cd7941191e21c8086f6f6fa89c674a5f9ab5353`  
		Last Modified: Thu, 08 May 2025 17:48:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d01ac7d87d757a91ab0cb1b2900d149fd09685bd39fc01c98f02d78ba2eb3dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 KB (135853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f217346cb64cb93bc59dfe6e53827b86a6b964768a4b1e143920f6c7bc5df687`

```dockerfile
```

-	Layers:
	-	`sha256:a4639457c7e3132443dee9039de23a76d3bc306d2582aa039fdd3a3ea02ec7ed`  
		Last Modified: Mon, 07 Apr 2025 22:36:53 GMT  
		Size: 115.5 KB (115498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6aad833b83ae49827a8d4b18fce8012f3b1e2ffe9cbf70bccd69e726b387cf7`  
		Last Modified: Mon, 07 Apr 2025 22:36:53 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:dcb073a98acebf299969b7ee8c7fea0f906e3deb17ce0a34525d9a53e89380c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be15ac2010ddae637baf33795cede581de71e4a4754e581c54a33d04f17f9d56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb6ce72b86df2d018ff01f4fb22b4e85430f57122af3f864ae27b1516152e`  
		Last Modified: Mon, 07 Apr 2025 22:36:04 GMT  
		Size: 2.9 MB (2894884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e419c26e35d3c729c835bf6cf63648185f464ca7e122d32e08add57cc006b51`  
		Last Modified: Mon, 07 Apr 2025 22:36:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:2b974df5b8052cdc19121279793a637ff2d8a2727282276889adfe94463c2283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4338d3d9f2d39a2036110eb9114acb29242ba1bef2e68d0dc4d293a2db051b4c`

```dockerfile
```

-	Layers:
	-	`sha256:1308525e0be456a8118bcbc459b22e43266b6f070c21443e338b2f3f7b79e239`  
		Last Modified: Mon, 07 Apr 2025 22:36:04 GMT  
		Size: 20.2 KB (20232 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:e5967eec28d8d64ba528b3edbb529b700103c21d52fd1298b9f22c57cb26898d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de59e8a62b5aa373c31245c8964d9fd98b2116dfc343caec813cca285b5dd596`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749f5969e0e2badabc3af23cd52a9ac830b7f638549ded33d201c6c542ce5e13`  
		Last Modified: Mon, 07 Apr 2025 22:36:12 GMT  
		Size: 2.8 MB (2847683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8064da4975b91cccc0413f052d45cf9ccf796581c924d5be1911cdc6d358543`  
		Last Modified: Mon, 07 Apr 2025 22:36:11 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:88e5121fa7a63d75eb0e3dc9eaafdb741327565d1dc265b2bac1e7b26402866e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 KB (135997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11710131f6237ca99a2dc7da97aa6083d872d4f7d91fd91cd38f139e0569e488`

```dockerfile
```

-	Layers:
	-	`sha256:82424dedf2fe6d3d75a70cabea5fccf26a065da6dcbc28f59a2a184e24f3ed65`  
		Last Modified: Mon, 07 Apr 2025 22:36:12 GMT  
		Size: 115.5 KB (115550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70911b357b4e45db26cf93dae1701e7181dfc88ae75b70eaeb9c87fed82d2d0c`  
		Last Modified: Mon, 07 Apr 2025 22:36:11 GMT  
		Size: 20.4 KB (20447 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:0aae13f2711183397080d579ac8a55e401bee875f0797c414af09bf57dea3b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3be3d087c477e61fcf3b009c401e683c41de89744f04697a8742bdca814589b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0965d44bdddab9136a40d1c2795e22ce68fe62df37bd2ddb3587ea145b40ba4f`  
		Last Modified: Mon, 07 Apr 2025 22:36:13 GMT  
		Size: 3.0 MB (3046418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8643de5a6d14913868d0ecc7225ec6cdb61cf7e634ec6a8e1abc9bc1443475`  
		Last Modified: Mon, 07 Apr 2025 22:36:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:5106349335c6239df90259faba1fd2f24aa326a6973c26bb7292fc8340bbd9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b31b3a54ebdd80ac7fed196f7e97739fbd05af499321bef69c3be8cf769fcf`

```dockerfile
```

-	Layers:
	-	`sha256:606b1202c9d924f7b7014d4b36f038884a573643dc19b1492632d5e95a1ee3f9`  
		Last Modified: Mon, 07 Apr 2025 22:36:12 GMT  
		Size: 115.6 KB (115578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3181b7a578f1b17646e370d1a6fe5914b74d590395a7ad10a6b56f18373cbddd`  
		Last Modified: Mon, 07 Apr 2025 22:36:12 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:a443520ddd492411004a7aa1dac69f25c1bc594ab2578b91180295bb41ce0793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6349782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f592682e8fef57dbbbaa290fa6b5142245bbd5e4787e2a2494061189534a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a395f41f86d8fbfbe79d146110cd80a517abe51a53d3d741c83831a737c5d`  
		Last Modified: Mon, 07 Apr 2025 22:37:00 GMT  
		Size: 2.9 MB (2885826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61355e8ba1d6bd603ed2e64409507049d48a08ac23b2b5f75ddd8208421f5f68`  
		Last Modified: Mon, 07 Apr 2025 22:37:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:77a496a9126d3f3f3354d54d9cb94d080c620ae2a59c6b3a2749346be76c9206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 KB (135775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166f91b5128ce73c945d69766686fb01cf7140dbcfc74c600c2750950e1b36d1`

```dockerfile
```

-	Layers:
	-	`sha256:19f59293e708318767f3ac12490a9baf214dcfa6c74425e33c9f91b6f089b431`  
		Last Modified: Mon, 07 Apr 2025 22:37:00 GMT  
		Size: 115.5 KB (115463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974ffc8476c33a210f93eb43e7599e78b4765015c2290c230076b94c10c7a281`  
		Last Modified: Mon, 07 Apr 2025 22:37:00 GMT  
		Size: 20.3 KB (20312 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:79ee9c3029444520ea58bafbf9f85298b2fb749b423a28b1ce12d3281690e8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6805702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4b97cdb0a0742c947924d7610bf78bb6d43348ad23fb35e1356ba2d3da7bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea05ba906185c79fa3f4875245344d93bea56e126150ee5c9756b72e69655f1e`  
		Last Modified: Mon, 07 Apr 2025 22:36:57 GMT  
		Size: 3.2 MB (3231020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fa20f846d437fe42ea2f0dbec0426fa412a954ea88369a8c868ac69cd44ef1`  
		Last Modified: Mon, 07 Apr 2025 22:36:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:1fcf86005647934996052356774af7981e14a3e6940a24a459e592f8ee79cb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 KB (134004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42de8ec491cb1a5a33d3e9146b39a4ac99f6d477d8126e6cf991d7471bb98411`

```dockerfile
```

-	Layers:
	-	`sha256:898fc0dcd723a31ad38cb5cbe2ca6b0f5548eebf3ef435278e0eb3593a70105b`  
		Last Modified: Mon, 07 Apr 2025 22:36:57 GMT  
		Size: 113.6 KB (113593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dea7a069430f07a169282362970d061d6c4ffb0e062a2d4ce4b644bb639689`  
		Last Modified: Mon, 07 Apr 2025 22:36:57 GMT  
		Size: 20.4 KB (20411 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:4beb83c971a0679d40442328aa4369952ee1627cfd1d854a97874f704cbc8553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6260990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb43e91ca50e3e3e6ecb79e3098b8118d288d12f91b58d8bd2cb5dfb9ebdf8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba0d2f6c430cbe61f0185de22d6c95218fd8624bf8e24b22401ac01689ca5a`  
		Last Modified: Mon, 07 Apr 2025 22:45:15 GMT  
		Size: 2.9 MB (2909212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4e83dc89534e721c49a0172d52fb70f7fe2ae660b592bbbe5c787f292f32a8`  
		Last Modified: Mon, 07 Apr 2025 22:45:15 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c0531de253ca0688285db44b83ee972d097d03d00a0af4e393d1e52372acf15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 KB (134000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a648c89b998e5dfed2cd6a760e1cab2093397226f9747e537ba0510de2a9f75`

```dockerfile
```

-	Layers:
	-	`sha256:3f855cf88ce54dd32402d2df9eea5d779c66d3792fc3270bff54dc31d67d19f9`  
		Last Modified: Mon, 07 Apr 2025 22:45:15 GMT  
		Size: 113.6 KB (113589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3598ad8326a490a64c4e448d275562b24bdf284caa390a34777f449e70696c`  
		Last Modified: Mon, 07 Apr 2025 22:45:15 GMT  
		Size: 20.4 KB (20411 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:c0f4fab3a7ea2c9659f76c680f307bac5ed7d4e1a4eb69a52a681cfbf43b4f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6523818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d115d83305f86bd029175116bc76e46cf5dbbac88d307d9b575458609b7e4a6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_VERSION=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
ENV _BASH_BASELINE=5.3-rc1
# Mon, 07 Apr 2025 16:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 16:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Apr 2025 16:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e42a493cfedc717508d86794e14f5051d62b919d80d3862cad49a3f1a2314`  
		Last Modified: Mon, 07 Apr 2025 22:36:21 GMT  
		Size: 3.1 MB (3055918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450595fda0906f988a7ed0213b01bd804fd4e5bf5a07e302800c0d54868ce1bd`  
		Last Modified: Mon, 07 Apr 2025 22:36:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:13b269604cb10824e48e5c2b1541a5c56787c37f1906196eecd102ab8a6220b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 KB (133902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d21daaf2f405bddfe1b690946f19d124373939c252027a866bc7c901df2fd2`

```dockerfile
```

-	Layers:
	-	`sha256:8aa3700242b5f0831c71edb1af51ba4fb854fb17ad0e3b4a005db48866985c06`  
		Last Modified: Mon, 07 Apr 2025 22:36:20 GMT  
		Size: 113.5 KB (113547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f25c2309a38c01ec92b36450ec2b120b804c6a1b14ae86358b6de52d44010a3`  
		Last Modified: Mon, 07 Apr 2025 22:36:21 GMT  
		Size: 20.4 KB (20355 bytes)  
		MIME: application/vnd.in-toto+json
