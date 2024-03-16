## `bash:alpine3.19`

```console
$ docker pull bash@sha256:55ff5760a70522a0e4122091df3971a28d2b38207303b37e9d0545714908d2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `bash:alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:e7e9ae199eddeefb891d985c979e64ae97a8d335539b6085ee7df3a1a0398309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6102890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb4e69a801b9c97062ec8c8faed746afba428a71c70ce7b280e0384aa536f1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104abb8d8f6886d8ac8096ba011f1c6f62140595d02e6b95ce88a5c83fcbacfa`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 2.7 MB (2693832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58723bf50cb1925ba71de3e3431269ee74bba18d87a295f86f2698404ae310bb`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:e280bc0c3fec059f5f2288c96640c6247755607a3458819a057d8f069ea101f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66004b302949e0c2f10ae11f3af7a06a9b237113b89ee509e5aee7161fe5c47`

```dockerfile
```

-	Layers:
	-	`sha256:fb3fc0f7c419c9ce497306ef3b8e70280559f95b8cc282ef0687d62bd3782a8b`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 111.6 KB (111606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4273e721be2e32f234203fd8b5bdab3c5eb43bac55998a679e28ecc96008ea6`  
		Last Modified: Fri, 15 Mar 2024 23:54:28 GMT  
		Size: 20.9 KB (20908 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:6986fbdf23ba688a081f6353dcc9899a70b2d218ecdeacf2f970105f777c0f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5802820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f098ba3b9bc4f49dd93465e041a1180dac73034fe3f2b99863682c3294d3d1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be7404975846a79705bc601df99d006344f58d71c9fff3701b2acf0f18645fa`  
		Last Modified: Sat, 27 Jan 2024 19:25:07 GMT  
		Size: 2.6 MB (2637086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9518cb7fd70bc1e463dcaa48c12806999eada535bdd8182da2e7578d77f20`  
		Last Modified: Sat, 27 Jan 2024 19:25:07 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:4854727787ff73351bff872f1953c357dbcf5f894446ee4470c4c22a6864d7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 KB (20629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054277e3b8a9a7828a446421ddb810031e96d0561f000bb4ca8692b29663bf7f`

```dockerfile
```

-	Layers:
	-	`sha256:9b2b3e38ed0e75418323d33de5d9497d07605311a26c2c19b04ac3e7473fc986`  
		Last Modified: Sat, 27 Jan 2024 19:25:06 GMT  
		Size: 20.6 KB (20629 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:e4a5547790eb54f5f3c29e747c50011392112cbd6f1dcc2d73993a4bcf76695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5509980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0572e1d3921dc2672c42dc5980f96c3ac9d13d7d50f4ecaa93ee30794e348a32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c84281d97d6604fc95df6a29f63a7ae0f854aa54a7a021beb70f6dbaadde5e`  
		Last Modified: Fri, 15 Mar 2024 23:55:53 GMT  
		Size: 2.6 MB (2590746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bff8586dca1fa362560a4274b4e63155b0ec476f0d88f41271040cc8fe2cf`  
		Last Modified: Fri, 15 Mar 2024 23:55:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c0544926d555279bf66b0288c441c9bbb0d898d1410afab23c238b4acda07bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06cad1152811b8160e5c53617b4ab5d7598a3a2174103aa44a17b6e17db9365`

```dockerfile
```

-	Layers:
	-	`sha256:aa19bb4f1a407ba2aa4a03fd348476b2cf487870a10876d21be0f36e8eca9196`  
		Last Modified: Fri, 15 Mar 2024 23:55:53 GMT  
		Size: 111.7 KB (111674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d87a3bed92a1990f1563eddbeba6346f1293c47771a0afd9e496329e5a4e17`  
		Last Modified: Fri, 15 Mar 2024 23:55:53 GMT  
		Size: 20.8 KB (20842 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:4945d23da9862dc7db8c8582d15885b445a8cd1379d3805d70692ff1c5be17eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6129594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0b7c7c3e41d327593839a619694ec708fadc1cfa9e639e7b226e485b5847a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7f1892fc445f004a86a96f6571455458b5d1e0bf0cf1b4442dd38bbcd7c4d9`  
		Last Modified: Fri, 15 Mar 2024 23:54:41 GMT  
		Size: 2.8 MB (2781551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08a5a04fd53ee4e10a4e28cf3f1165df10bb98cc9fef6c536c76c16bd963c27`  
		Last Modified: Fri, 15 Mar 2024 23:54:41 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b0a141ce560f4c57679049b0b4a770f9541c5bef5efbd1a16409bdae104eee51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 KB (132385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72503da291d99113a9df4aa29dd953bd735002d396017d57e1baab91bbcd7a3`

```dockerfile
```

-	Layers:
	-	`sha256:bcb531e75f6c50d75e8a05d90bd6edbe580c2b741538e4aa0300e81e1e4f899d`  
		Last Modified: Fri, 15 Mar 2024 23:54:41 GMT  
		Size: 111.6 KB (111625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6a96a6c1f1a26dbbdbddc3d0ecaad506087d2205fddef747879b47b484693de`  
		Last Modified: Fri, 15 Mar 2024 23:54:41 GMT  
		Size: 20.8 KB (20760 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:587e216cad6476f7931376af499e4501d0d53f72ae451824931a6f76fc7d5dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5888762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef820f7768868d24b320a56860ee0af1dadaa1336ec5ec72a7e45a3ada0ab9ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541951b1204eeb33cd06a7b4e524d3c986202d93c936f0893cd21db148095a66`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 2.6 MB (2644342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aadc9c7ab835a899f250783a49eb823231df70aa421c6999dd0d7218d36f82`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ad2f3279453f2cee4e8389912c7669d8ddbd100392193562542cc46d18848f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 KB (132420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75878e88dad3ca2ba1186a9d5dfcf4efbf3a5e9d48b8f2eeb13ea2e996238a1c`

```dockerfile
```

-	Layers:
	-	`sha256:341945d94dcd23dfbde476a09309c8ba9f59d486936c4b900aec36c822053e4c`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 111.6 KB (111561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d210260f5e847d57a8948deea6ab15c6506feb5e7b2c7d6bc7e785ff0337acb3`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 20.9 KB (20859 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:fd3c18c0b4bfebdcd32dcde12d910fbea0c2c0e9ce0c1e27052908a64d871a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9d9437576940131ff47dd4e2404617bb2d1a95b1d3d22ada1f77d8d4350e1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97850dace65dda3171bf346b84a8062f4536fc6db8c2fe856c261b7d95fb9be0`  
		Last Modified: Fri, 15 Mar 2024 23:55:24 GMT  
		Size: 2.9 MB (2945384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bfb2f445014c7c7a18ffddd94926ae6acc8154eded3a7290802b98ea65f236`  
		Last Modified: Fri, 15 Mar 2024 23:55:23 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:1ca819c6d0b0ba4e0515a16d5e969c8da03cbf5865fd7032f8c440ca0a93b9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 KB (130514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b9126181ec32e215d5cab180dd245ea65294c2eccbc946f8bb40e6a90b038`

```dockerfile
```

-	Layers:
	-	`sha256:5cfb5fb706d6da5440bf3ea3eb275d2801bc4a465f52902a2c704da0aeda8d0d`  
		Last Modified: Fri, 15 Mar 2024 23:55:23 GMT  
		Size: 109.7 KB (109710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f71932e0baa7a218f88eb02fc28bfb73e7570c33a3d9a23fb9dd9898f6e9bcb`  
		Last Modified: Fri, 15 Mar 2024 23:55:23 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:c3bfeb62c13371ff3185f414ee07ca2c9c8852a07b8605564f5e46313925d685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6024744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2539b8b99d4cdbb554667be6d4015b5038a43b3972ed580d35478d2d6b86df6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 14 Jan 2024 05:17:51 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["/bin/sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_VERSION=5.2.26
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE=5.2.21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_BASELINE_PATCH=21
# Sun, 14 Jan 2024 05:17:51 GMT
ENV _BASH_LATEST_PATCH=26
# Sun, 14 Jan 2024 05:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "$_BASH_VERSION" ]; 	bash -c 'help' > /dev/null # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 14 Jan 2024 05:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 14 Jan 2024 05:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773523f073c1f586ce2fdc70c56d3e4332aeb3e6789c0abed80eeb7435f3f280`  
		Last Modified: Sat, 27 Jan 2024 20:18:50 GMT  
		Size: 2.8 MB (2781773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979958642450231a1712504bf7382ad3be30e03b4ba5b573c70de9f8f72bf4b1`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c025d13613f3b48e79d9dcb1b429121e297e784af489cb30887c0137c0e429b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 KB (117992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb7a87e436a0c220e831128b54965bddc540a6dfccc61e2e635ae4fc46002d6`

```dockerfile
```

-	Layers:
	-	`sha256:7884a36e0c3e05d91addce80cef7e850e9bfa70ecc3d43cbc6314492266acc5b`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 97.2 KB (97250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecbfd5ce7bb50d347b5fa5369d002de1ed6a45f11247aa46af607461b6247a64`  
		Last Modified: Sat, 27 Jan 2024 20:18:49 GMT  
		Size: 20.7 KB (20742 bytes)  
		MIME: application/vnd.in-toto+json
