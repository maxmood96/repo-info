## `bash:rc-alpine3.22`

```console
$ docker pull bash@sha256:6ee6cfb2eed3bf295783dd810fee4fd3af808561138f971c047b0dec312c34e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
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
