## `bash:rc-alpine3.19`

```console
$ docker pull bash@sha256:82c93931bcb3f65780e4e2e1ddf2b3b0bffcc93e30e581f151941cb25a4a51ec
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

### `bash:rc-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:e8634549ac795bc4e2c15ac5a59e2d8db734476c553f1f0517b0432e1a0284ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6295987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9cb3eeefc53985a1b1c8f5a139f160663e8cd7ad27199b2c3b3ec87e6a543f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5bb3212ddf6874cb49c639d5604c424876c7ae24f1bfd04ae6629a6f89c2039`  
		Last Modified: Tue, 23 Apr 2024 23:51:05 GMT  
		Size: 2.9 MB (2886924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dda98164dca90d231b6cbef8665208ac85db656b8fb48ed67cfa57d0c44b8d`  
		Last Modified: Tue, 23 Apr 2024 23:51:05 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c388aab3a79cf87084fa8123f09de74839d79960672f5c0e23001c34d9be21a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 KB (131215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e8ab314b0a628133f623fe09b84fd0043683168c0d158901150efe0fc6cd3d`

```dockerfile
```

-	Layers:
	-	`sha256:30d7c361adea5f4ec77dd22c8034e271a507314e47280bf8734b5a50e5bdd27f`  
		Last Modified: Tue, 23 Apr 2024 23:51:05 GMT  
		Size: 111.0 KB (111036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e70ab53e1aa0b8fe3e9274b43ebfe0c5dd03d612afda345cd2a11d70339bcd`  
		Last Modified: Tue, 23 Apr 2024 23:51:05 GMT  
		Size: 20.2 KB (20179 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:29559e5c0e4b687cba5242b28b7c47c507900fc2eab01c9573dc945818d19fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8696a219ec660a1619f4c910a234d1fbcb799a2019411a72b7dff4a876b40683`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709f9326f1dfbfa159e9fad960e821223c3d0c05132c5ffd8ca072bb2c7b8008`  
		Last Modified: Tue, 23 Apr 2024 23:58:21 GMT  
		Size: 2.8 MB (2839341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a860d80e5f20d23009e897512ffe8e14f8df949f4eb209707c2bb89346a13615`  
		Last Modified: Tue, 23 Apr 2024 23:58:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:fc72bd2e6021075883aff6a17b97bf3b2c5170d60372c67a183916c98729bcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 KB (19880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a7ff1a9da3d390ce35f4a2587537c64c40ccddac21ba7282513bc0020d2e37`

```dockerfile
```

-	Layers:
	-	`sha256:56138e0efdfd35e695c630698f64ac65f32a87493f86c1e9eaccf60a0c39c8d5`  
		Last Modified: Tue, 23 Apr 2024 23:58:20 GMT  
		Size: 19.9 KB (19880 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:c5a91a9d584a11c821222cfe723841504b2ac1e5c13555610798ddaf90ab184c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e516c323beb007cacc827590efd14383406a944b2179d16d24aa7373aa7d80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373487ec3ccf9550be3b7cd7008a41c7d818db1c36894c416e9421b9ccce71ff`  
		Last Modified: Wed, 24 Apr 2024 00:22:51 GMT  
		Size: 2.8 MB (2783983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40c4990855f43a552b5656b69d12de4673b80234b53b60c60e4c0a489de2c6d`  
		Last Modified: Wed, 24 Apr 2024 00:22:51 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:26abfe1687e6d6e62edf9e6ccc7d6a76a39c9e5273704b40e5465cbf145cdfe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 KB (131187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d06e60f052258c44e247272f94a3ea096c324243be805b57b7d01fd3fa523e5`

```dockerfile
```

-	Layers:
	-	`sha256:89c2662a9bad43e72f503db94907ddf416217780f53304556a3ab6c2bbafa315`  
		Last Modified: Wed, 24 Apr 2024 00:22:51 GMT  
		Size: 111.1 KB (111088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e8239b30df781bfac58bd0ea011dbbb25224b4b83c0ffe7c291ab27383bfde`  
		Last Modified: Wed, 24 Apr 2024 00:22:51 GMT  
		Size: 20.1 KB (20099 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:e3fd3c9d6ff41c12a17fbc7e9af21d796c71d49333ce291da70736bf56e28857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6337926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfdb786731b92556062e795b260af4a3a96b611259b223a74c70d0ab0c2e3e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1761da7784235d100406e5a4b0a615e314b6edac8a50ad8e50526c48b102c68`  
		Last Modified: Wed, 24 Apr 2024 01:22:05 GMT  
		Size: 3.0 MB (2989875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d4978246c279f9698d67903d6bdaec1e03cef5fef4c948cd9c10757abf2e8`  
		Last Modified: Wed, 24 Apr 2024 01:22:05 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ec8c49a32544f01c539a11d923a7ab79b9297d7f419cdb43875f9decc7f61677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 KB (131078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad26a47a40db046370f94d3c5464fab06c6fa76f8fb3d9804fe404bae226289e`

```dockerfile
```

-	Layers:
	-	`sha256:a9ca8634c464881a60f5fb4acf26ede9b2d01879aff57d3aa0f7e0efa32f5fe1`  
		Last Modified: Wed, 24 Apr 2024 01:22:05 GMT  
		Size: 111.1 KB (111051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2baa679cbbaa4689f32e945b731bfd033a103ed64f0954a63663943c62579d96`  
		Last Modified: Wed, 24 Apr 2024 01:22:05 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:36acf44b98250febee9a94cf6947d7e824f37b69678b16226df0773bc766da00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6071027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52c78e0dfdd55dfd07d2938b753c80dd1ba4b587305eadebaf4c4a485b876e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec55da73859e8525802dfdb6e0898a4a378a79235544f9c3fc69af7b186fa0d`  
		Last Modified: Tue, 23 Apr 2024 23:51:09 GMT  
		Size: 2.8 MB (2826600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59517aa370fa74203a3f6f8747cba677956fabca684ef4099c82e1f8ebe2660b`  
		Last Modified: Tue, 23 Apr 2024 23:51:08 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3da24b6f8e968b646505398d02e81733aadfe93d45c673a9bebd0ac9fcdb7369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.1 KB (131141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3959cacb2f9ab9cce618dcdacbff12bc63473b21899af2d726b6349389242ae4`

```dockerfile
```

-	Layers:
	-	`sha256:d16b56f06bce29da9eecabdd6f2601854d3cc61ae8fa2fa4eec851e56c4c4344`  
		Last Modified: Tue, 23 Apr 2024 23:51:09 GMT  
		Size: 111.0 KB (111001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266b99483696d56243bfee16e625b5378717e0b26fa48ff9fd712d819ba32957`  
		Last Modified: Tue, 23 Apr 2024 23:51:08 GMT  
		Size: 20.1 KB (20140 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:e7b4f984653abdc6c1a9b53bf912845b562faafd60071282af9cbf1544f2f3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1a22852e99de42e1485cfc788b5fee1f2d7f71389115005fa5ed08517e3160`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8a40b69264c0658de3131304e71d64ecf7341771c6309fccd26b172b900078`  
		Last Modified: Wed, 24 Apr 2024 00:16:26 GMT  
		Size: 3.2 MB (3158464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b69b2f5cf8d72f80e80c25f494572d99eb14ebd664abe58e9eb68abc31c3315`  
		Last Modified: Wed, 24 Apr 2024 00:16:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:46ba83296b16ae015f469ccafd7343937d2ceb2f47c988c73d53750fcf86789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 KB (129191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cae8bc8c843d0f1df11ae512cb385dbfb2e5584a140ce7430be84e954fd1e`

```dockerfile
```

-	Layers:
	-	`sha256:306a5fb8b20952a295a89f909249ceba07cd3dbccf12b18d4ec121d3de946eba`  
		Last Modified: Wed, 24 Apr 2024 00:16:25 GMT  
		Size: 109.1 KB (109128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a2d93e33aff6bb47ec82c3b410d52b369e225833f06dc71b0aea92fb19823d`  
		Last Modified: Wed, 24 Apr 2024 00:16:25 GMT  
		Size: 20.1 KB (20063 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:rc-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:3cd80c16d68c19c873af78ba2e8caeaf4914e27c9ebc52f9b52d79849f440efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd813fa390c6d388ed05eada2d568f26e38e35cb77275fa908a579c9f4b5eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_VERSION=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
ENV _BASH_BASELINE=5.3-alpha
# Mon, 22 Apr 2024 20:48:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz"; 	wget -O bash.tar.gz.sig "https://ftp.gnu.org/gnu/bash/bash-$_BASH_BASELINE.tar.gz.sig"; 		: "${_BASH_BASELINE_PATCH:=0}" "${_BASH_LATEST_PATCH:=0}"; 	if [ "$_BASH_LATEST_PATCH" -gt "$_BASH_BASELINE_PATCH" ]; then 		mkdir -p bash-patches; 		first="$(printf '%03d' "$(( _BASH_BASELINE_PATCH + 1 ))")"; 		last="$(printf '%03d' "$_BASH_LATEST_PATCH")"; 		majorMinor="${_BASH_VERSION%.*}"; 		for patch in $(seq -w "$first" "$last"); do 			url="https://ftp.gnu.org/gnu/bash/bash-$majorMinor-patches/bash${majorMinor//./}-$patch"; 			wget -O "bash-patches/$patch" "$url"; 			wget -O "bash-patches/$patch.sig" "$url.sig"; 		done; 	fi; 		apk add --no-cache --virtual .gpg-deps gnupg; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7C0135FB088AAF6C66C650B9BB5869F064EA74AB; 	gpg --batch --verify bash.tar.gz.sig bash.tar.gz; 	rm bash.tar.gz.sig; 	if [ -d bash-patches ]; then 		for sig in bash-patches/*.sig; do 			p="${sig%.sig}"; 			gpg --batch --verify "$sig" "$p"; 			rm "$sig"; 		done; 	fi; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apk del --no-network .gpg-deps; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	[ "$(bash -c 'echo "${BASH_VERSION%%[^0-9.]*}"')" = "${_BASH_VERSION%%-*}.0" ]; 	bash -c 'help' > /dev/null # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Apr 2024 20:48:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Apr 2024 20:48:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3a9ecdac6064b5a5e2d9506680a2e5f44738efcc92e5c9d2cab850e14db6d`  
		Last Modified: Wed, 24 Apr 2024 01:32:19 GMT  
		Size: 3.0 MB (2988619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecac9771785a1ded6e3dc6446627d8a292e2cd9967bf7b49362bac2d6347db56`  
		Last Modified: Wed, 24 Apr 2024 01:32:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:rc-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:aaed7f17fc0c5316b50d7cc9cdcd6be65ec5392a84f6c81f83d970b3be11a71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 KB (129095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b553777fb60d1c02dc25a4d1085c28b2fc68f7079808a4287964cad5d5fd27bb`

```dockerfile
```

-	Layers:
	-	`sha256:de7fad2ecc558e3856680029f299d4885f9811d7c302e6fba36465ed58cfae69`  
		Last Modified: Wed, 24 Apr 2024 01:32:17 GMT  
		Size: 109.1 KB (109082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1b918f475c3c9bbd8e6e92cb92ac801ade20405a060841d12b12f2184145a5`  
		Last Modified: Wed, 24 Apr 2024 01:32:18 GMT  
		Size: 20.0 KB (20013 bytes)  
		MIME: application/vnd.in-toto+json
