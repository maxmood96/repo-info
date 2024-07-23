## `bash:rc-alpine3.20`

```console
$ docker pull bash@sha256:ef1cf433ccab3db117fe78aef2d9c29bf2c774d4a4744d06deeb3f91729988e5
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

### `bash:rc-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:7835412c9ecc16f516ccb3bbfcda714f1d07fa792830ff820b0953e5989067bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6509341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ccee4bda33cf3d1193b6f9562786b8f990b26eaece05ef53f9964a427981d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
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
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce39a2a07981639660df63255ac807fd48f143ab1cfa6e687e3f9ef7c29d6b28`  
		Last Modified: Mon, 22 Jul 2024 23:03:45 GMT  
		Size: 2.9 MB (2886114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b89e18a3a8e19c842b26023772b728710f9472765f91c10b854f67d838aad9`  
		Last Modified: Mon, 22 Jul 2024 23:03:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8e61fab7e837a47e4c14c4368a07198414004d24f45303e4ab1cc1dcf2e721b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 KB (130522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c3ad6556d30da17dd8ae0c93373e490af02686f63e863654a10d125dd67157`

```dockerfile
```

-	Layers:
	-	`sha256:47748fa77e4409916e34f90b0d480c96c32ee58947acd6687635110cb62a996b`  
		Last Modified: Mon, 22 Jul 2024 23:03:45 GMT  
		Size: 110.5 KB (110461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff2bccbfa584c8d83e86c9702b7649dccca57649eb5a491c9e41ff751ed4712e`  
		Last Modified: Mon, 22 Jul 2024 23:03:45 GMT  
		Size: 20.1 KB (20061 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:723308fd247d185a6d23525dc600b4e01d199f983f7aad9cb92f263a290b6553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6202980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7276e7962536b8043b392ef3b2c4159383cae5d449e1b324af099cb25322cc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
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
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db3a0ceb7c4d5d4960cfb1d19ac522186770f8c15422ce5da2f018cf9a7102d`  
		Last Modified: Tue, 23 Jul 2024 01:22:11 GMT  
		Size: 2.8 MB (2837457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c140177577310d5e06d70433108a01ee45562552e2f8a4788a776c9f2413529`  
		Last Modified: Tue, 23 Jul 2024 01:22:11 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:6822f86c7939c22e07e382d974b7c30e0c60767af2522f0599bd548eb4624542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00863370287fda3b29d195616cd1a768d2cd22bd167ad40dead7ca940492f12`

```dockerfile
```

-	Layers:
	-	`sha256:eda29fe1caf33d0ed32769fa177c5c8866b74e51a5381ae7fc248a0a80e440ae`  
		Last Modified: Tue, 23 Jul 2024 01:22:11 GMT  
		Size: 19.9 KB (19929 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:4ce5f20eafb2939d72d1822c819ef527a607ac4ab873775886130dd80da13fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a64223ce4a9c100ade416f1e005375f02516ec0b2e0aba4bd6011fd0a962b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8535de2759ed12b5e986ab03201d87ed6d6f7e569c8ce7c1c4745cc27b35056`  
		Last Modified: Fri, 21 Jun 2024 02:24:50 GMT  
		Size: 2.8 MB (2783098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f60892d7bcd93431bfc2962bf79b4bd0809b1bd92f1605b778d25915d309d6`  
		Last Modified: Fri, 21 Jun 2024 02:24:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7249aa4d6526574aedbc02013414361411782f3efd6b83632e53af09f5cc5d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 KB (127287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e2ef569a9453f415084e9cf369db086677bb81525806d9296df801cd804b9b`

```dockerfile
```

-	Layers:
	-	`sha256:b510355bef09e84b77337867fc03f4dc19854652dcfc46afbabd54940eb7845a`  
		Last Modified: Fri, 21 Jun 2024 02:24:50 GMT  
		Size: 107.1 KB (107139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209fdcc8dda656b402d1f79484c18b9b92d4ceb06da06be64df1737458aa40f3`  
		Last Modified: Fri, 21 Jun 2024 02:24:49 GMT  
		Size: 20.1 KB (20148 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.20` - linux; arm64 variant v8

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

### `bash:rc-alpine3.20` - unknown; unknown

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

### `bash:rc-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:046c4dacc1d224bf5b8b873707d6c3136026be73d92fac4724404da68c84ca83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6295085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4516029e294b7e7a385c76a43d83a001922784ebbf33007e2bb2a3ecafa158a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
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
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274acfa53e3a7e329a1daa8806374314c68142716c369951dbfc18829a6c225b`  
		Last Modified: Mon, 22 Jul 2024 22:06:56 GMT  
		Size: 2.8 MB (2826677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3261588e07e46be86ed88757eb7f31cde962e928235658acec024eca6e0b9b72`  
		Last Modified: Mon, 22 Jul 2024 22:06:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d335de24dfc5d5aa8e66605ebdb5e566bffcc41079a3a7295226f19a481558cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 KB (130449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ae3f0577930047e5f0488a5123f47e149f1bec9ce3d07d7eb4618446b557f0`

```dockerfile
```

-	Layers:
	-	`sha256:81dd5a7bffe7231f7a67dcc2e1fee0d37d94ad58854c568d63009b20dc6c2101`  
		Last Modified: Mon, 22 Jul 2024 22:06:55 GMT  
		Size: 110.4 KB (110426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6a41a98e616dfcfd869b694b91982195d6a46ff30ef2629867a46a8681368e`  
		Last Modified: Mon, 22 Jul 2024 22:06:55 GMT  
		Size: 20.0 KB (20023 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:b36fcb929a90261f32099e5add4d264565cb8973479f49b21f1102c6f84f33c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6728695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec18fa47aec127db8bf4d1bcefd8dce9e345823c7d58e3371eaab4cf3b2297d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a34ac2c9befb58d2895da0d5881b50e2b3c8790538ab2b89135dd694cd05be`  
		Last Modified: Tue, 23 Jul 2024 08:13:35 GMT  
		Size: 3.2 MB (3156802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60caa4688bfde6280e08476fae39098a192fe0a56b878b0a3f1303f07fd380`  
		Last Modified: Tue, 23 Jul 2024 08:13:34 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:aae75cbc7d0061cec8070611f71e33e2341181da1b97e2a038550e858ca936f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 KB (128665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5ad4baab7fb933263eb7dd98e28d89944a2528101187a08fd7180b85ca54ba`

```dockerfile
```

-	Layers:
	-	`sha256:5631d28180d4ebf3a683620414b87ff524eea455bef3b8ee9643a6eb2d5a6487`  
		Last Modified: Tue, 23 Jul 2024 08:13:34 GMT  
		Size: 108.6 KB (108553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2677825d36ee5495cd21d230faf894c28bf95df3a05d970d7b823060f5821865`  
		Last Modified: Tue, 23 Jul 2024 08:13:34 GMT  
		Size: 20.1 KB (20112 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.20` - linux; riscv64

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

### `bash:rc-alpine3.20` - unknown; unknown

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

### `bash:rc-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:59ad7a08f119c2c79107416ce4001c3f757e1b40a526330d86f75e308b2f2d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6448403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efba5ad4795f08a7202ba6d79836e24214a100c83b53517efd8c465c39aba1f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 19:31:20 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
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
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6283017481a7fe0183bc2d943883e6ca6d141ea5f049d8a4142f855a1cfd45f9`  
		Last Modified: Tue, 23 Jul 2024 06:35:26 GMT  
		Size: 3.0 MB (2987001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baf1dbaa67893518007e7899567d67d1cd2699286260f9f3bd548ec62ca60e1`  
		Last Modified: Tue, 23 Jul 2024 06:35:26 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:9479d6322b085eac51170484da36ffd0e056285b7e8d8958558efc7263f46cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.6 KB (128569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732c2ec87219ae65a0416c296f24537bf59ad04c6eda7e0609ea78adfa05c086`

```dockerfile
```

-	Layers:
	-	`sha256:7181a6524f8e0d836e2d5e290b32f7487d1a3e4f67505e4b862c15dc290bc0f4`  
		Last Modified: Tue, 23 Jul 2024 06:35:26 GMT  
		Size: 108.5 KB (108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39f5d135cd16069416dd7ebf391e2a7206f75fca58dbf5fc2c9e525764c6869f`  
		Last Modified: Tue, 23 Jul 2024 06:35:26 GMT  
		Size: 20.1 KB (20062 bytes)  
		MIME: application/vnd.in-toto+json
