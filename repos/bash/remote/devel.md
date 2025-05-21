## `bash:devel`

```console
$ docker pull bash@sha256:f14ddf5b5320368f769cf61aa92a784a8206f5fea48c248be705fa2c07f71ecf
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:0344e5894c5468c1b2da51b1c95b570c42a2a6b85edd472f60a212ab7a366d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23440773525e47bc8c948d7f27d5b4e697ea99a922cfe6c125ba34efdbdc172`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f102d75825274b1b1523b56b5d4d6c4c3ab6b06e418525d4743134b71b4b4da`  
		Last Modified: Tue, 20 May 2025 21:38:21 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad16facb3c42ee6d45f56ab197807154b14db846bd345186ace2fa83668fe4`  
		Last Modified: Tue, 20 May 2025 21:38:21 GMT  
		Size: 3.0 MB (2996169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c25c6e9306920a7b736f92e9bd6da1a72f4eaf8fbaf7c3570996353648da2`  
		Last Modified: Tue, 20 May 2025 21:38:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:86aaf297c8d5da08c160a5ad17da840f5615a955c8ff5423bd7dac92a5716405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ae8b6217a412a77d83ff537261bc31de35ff9c68085b69f47e03374d1a1be0`

```dockerfile
```

-	Layers:
	-	`sha256:68cbf587ff6adcd3fd416369e96eb41f1a4b3b98eccbd384b0e309d05c8c2125`  
		Last Modified: Tue, 20 May 2025 21:38:21 GMT  
		Size: 116.9 KB (116875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc6a8a3397a2098d867986353595a27aa287e71059fd528c1e07674f1fb2925`  
		Last Modified: Tue, 20 May 2025 21:38:21 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:b48ccd762a3149105980eb8b342f7ba9e5ceb3df40f757dd412144d4440dc90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6297603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9866e2e2d20986dffc90a1e8e731880905e20c821472076236880cfad208c613`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f71d03b79647836cd876f54899ad58fcddbbb6e8b09ec300fc132bd64af9c6`  
		Last Modified: Fri, 14 Feb 2025 19:17:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a00e958e6b4ef8e2a9d7d3b45c76237453f3972d55bd7a157126d16a15745f4`  
		Last Modified: Tue, 20 May 2025 22:03:55 GMT  
		Size: 2.9 MB (2932075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dea8c3d7d033054f6fd8a756a8ca27661b3ccba74441e2df73f943ab6cdcfe3`  
		Last Modified: Tue, 20 May 2025 22:03:55 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0ba3bf89111571969eb36c27ee067ffbeff8d7483509f35989bcffcd8a5fd0e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac001d130edf242d338b7a19a1d9647dee279a2dd45c7ecb928adc24c6ea9663`

```dockerfile
```

-	Layers:
	-	`sha256:ce93c3e81af7c1c950beaf48ea4b1994ba43e95eed774b457558e74cbfe1dc2e`  
		Last Modified: Tue, 20 May 2025 22:03:54 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:b165de208f58c5c79dc87c1661d3c6865d7b1417e976a0c5633abab08a860b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5980871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9877290a05ecb6328bb8ea02cc9f8420eea7b808c45d90f9d2af23d628eb1d55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b71f74feee41903055522dcbbe45229fc23ca960d7e80c99f2747b60a0a3b1`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe9f24d00ff075598f982d3cbec64132d45773674dd9a32e386376b82b26a70`  
		Last Modified: Tue, 20 May 2025 21:37:46 GMT  
		Size: 2.9 MB (2881960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8bec46d89099e75ea1e511639daaa25e1ff170ceea692b363ad7c155363714`  
		Last Modified: Tue, 20 May 2025 21:37:45 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2b6b4f8e9ad2e454e6134a0d8f6de3f5769b51f9d8fb4bb8f40752fefcc1aa27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911c39b12c690e1cf1cdc3d0c34e85175ac7dbda5c7e86bfceaf499630865218`

```dockerfile
```

-	Layers:
	-	`sha256:995eedfd3779867da5b23f823be24957fdf5cd42d8e49f6dcc3e9c11e10077d8`  
		Last Modified: Tue, 20 May 2025 21:37:45 GMT  
		Size: 116.9 KB (116911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e147e1c1e2a28ca1a090703aba7cef3680e93302c1682b0d1e311d5d2a048800`  
		Last Modified: Tue, 20 May 2025 21:37:45 GMT  
		Size: 17.8 KB (17777 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5e339539f1130b76fe89a71ec7408905625ffdf0da5a67ba0e24769b58d167bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2362591591803b3c76a3f5c56ab09cedd01c29e4a2cc961716a01f1e534088`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f46bb25264bf2d21e412840d898d439bd2e303048a8d131f049fd47e15c1eeb`  
		Last Modified: Wed, 30 Apr 2025 01:58:40 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156bc7e5ae529bfcec847ed6c0cf0798b44839476e8ab8e5b61868f0f576c735`  
		Last Modified: Tue, 20 May 2025 22:08:13 GMT  
		Size: 3.1 MB (3082219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cd9c1fd909f7a649a45d49e9c7944894685bc7f3e01319c70ac8d1385e5b2`  
		Last Modified: Tue, 20 May 2025 22:08:13 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:bbeaa3af916fecaad4d57e19ed8343b1e60c402bfca51c3a7c2b6334a1c322d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de9e03d8b8680a8ccc24d9e7e5306a8ebfddf8e278a63db7f487da10e9e9ead`

```dockerfile
```

-	Layers:
	-	`sha256:a889f6907d018015245343985d7eea359cb1cff469a78b687d9fe082fd196e7d`  
		Last Modified: Tue, 20 May 2025 22:08:13 GMT  
		Size: 116.9 KB (116931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94927fa781c0409540cfca4897e6c6f8cade2744266926cd10eea039b8fa262b`  
		Last Modified: Tue, 20 May 2025 22:08:13 GMT  
		Size: 17.8 KB (17805 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:528a9ac9c6637064e32b8a318bb19a4860f5ee172b57306385e878047702c89d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f5a8ca70444c8f0b0b58a53596acfb42989b8e6c2e55d874a3704911bdfba4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3830c04d42fe0af25e95ffa37f28cf2db6e0e4a20cd3be74282fdd5477cfd134`  
		Last Modified: Tue, 20 May 2025 21:37:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7182475efe451a46c2003c1dae93fc40cba4cd4a7da613b79fc87ef46e12e0ff`  
		Last Modified: Tue, 20 May 2025 21:37:42 GMT  
		Size: 2.9 MB (2922922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3505a8b7116c0de4b65d379e8a24721fe347d9eb34f5fc2e33d71c73b0c0aafd`  
		Last Modified: Tue, 20 May 2025 21:37:42 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:804d2e6af693b28ec5083d83827f86da2fc0f027ca41d464a0c6866dfd136eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb205c65e19bc335f72e577175bef4b1684a58b03d2e206d48940e6282954a46`

```dockerfile
```

-	Layers:
	-	`sha256:d17f6f6678b7f3698334acebc0193d8eeffa3534b424cee24f9887a2f8a9292b`  
		Last Modified: Tue, 20 May 2025 21:37:42 GMT  
		Size: 116.8 KB (116850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1e8c108c17d38b4edec8b00e6e159fe56d8d06802a6d3ac3d13eb4213b1db6`  
		Last Modified: Tue, 20 May 2025 21:37:42 GMT  
		Size: 17.7 KB (17669 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:1fe784f4e03da30e7e5bd771336a482ae86c3547879d8f02e9d89839ba33f104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9269f8cfd179d69836ac7999fc51befe70944cdb8097ef9dc136cdcf1dd5eb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d400c01bd14c64fd11d69a0922ddce95535ebc6421198af720e8fe591b191f7`  
		Last Modified: Tue, 29 Apr 2025 21:15:32 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6228b142d42d8db71157e3c12587204162383278e606ce69ccbbea3a979ed8d`  
		Last Modified: Tue, 20 May 2025 21:38:29 GMT  
		Size: 3.3 MB (3271386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d96dec8226f3a0f215b741e07bfdd25fae4a98d16e2977fc58fb46ff08e7bba`  
		Last Modified: Tue, 20 May 2025 21:38:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1b065d0b783339095308b2bf65dd1235526e0aa1e0030f197986b62a74949718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001e6c056de2459aeec4796d171425f712c1f37dafaf52cf23f9f14d01651c75`

```dockerfile
```

-	Layers:
	-	`sha256:2cda7c41c18de57d874ac1c87373568c55f8952dbac8e1fe6fb9cc96d748cec4`  
		Last Modified: Tue, 20 May 2025 21:38:29 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3267737d2228f12961500c700c35b5294617df4f94acb1365e8c4130865f5303`  
		Last Modified: Tue, 20 May 2025 21:38:29 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:65d3c44f71fad3a667e123445223bb6c417626d432580b581955bce6c8e68b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adb90c9d80e37d53e2525ee75606e5fc92fda1630e359c4dee9da24a2546575`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03589e78b235e506dafea1c4a2d73b5326f0580bc335cad463e8b5863a7e527d`  
		Last Modified: Fri, 14 Feb 2025 19:22:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12656cbd70eb94865d6d8783c0ab3a9509b7468d6ce5a7e174c7878c42b13c4c`  
		Last Modified: Tue, 20 May 2025 21:52:05 GMT  
		Size: 2.9 MB (2944526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaaf035346a83ae1b725876130eb69b2bce9fc6d2d0a16299633cfd4265b3a8`  
		Last Modified: Tue, 20 May 2025 21:52:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5bf2e3496e3fdb4f1e7428c05ec9e7b7bf04a4891f94579c83379d172129827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66fdc2c151ea592bb9d3c629784b1ff320a40ff5d6c4d2cd3886a96bd3f19c1e`

```dockerfile
```

-	Layers:
	-	`sha256:fa1a75cbbe7ff8c30ea8af2ec3f2689fad06f17b0872f66ff2931d87c6caed54`  
		Last Modified: Tue, 20 May 2025 21:52:04 GMT  
		Size: 115.0 KB (114954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0afd3df7b13f29209cbc2275fa085b4383e8e1b90497cb139256f3171b7b50`  
		Last Modified: Tue, 20 May 2025 21:52:04 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:ffd09f53fd23df597a8d471bc21f60bf332a5e41c152d6f0ea04e07cad0eac3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ef93bc29d91ad92be0f067b755cd1b67025194455343360eb2c916b9f067bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_COMMIT=870ad4c92b771aafe5b444792a8fa904b2d4a418
# Tue, 20 May 2025 04:18:08 GMT
ENV _BASH_VERSION=devel-20250519
# Tue, 20 May 2025 04:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 May 2025 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 May 2025 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 May 2025 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f46b3744fb8a924c16ec91cd49f225382e9dc9803fbf9234c27869110fede6`  
		Last Modified: Wed, 30 Apr 2025 02:20:40 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a820889734d072f17595e259744bff264a9f966c57813beb3fec674f398a218`  
		Last Modified: Tue, 20 May 2025 22:08:44 GMT  
		Size: 3.1 MB (3091695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b5510bb11625ebcfd861656adee58679f3ca1bbbc4ba0e06f31dbbc33d6278`  
		Last Modified: Tue, 20 May 2025 22:08:44 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:84aaac3f8d1412e8c308e0bafd0c51ce4b61b102bccea2b31ff411d9f3e64972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff6eee117c5503071627f7bec1f00308b1b02902f6f07a1776554a385280a4e`

```dockerfile
```

-	Layers:
	-	`sha256:a528c2a262a3ff67fa73ba7e156cfc5635686c35760020c357d3b35ee84450e5`  
		Last Modified: Tue, 20 May 2025 22:08:44 GMT  
		Size: 114.9 KB (114924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef8a2832af1ebe0976387db63580801ca1df58354f59f2a2c5960724f343bc0`  
		Last Modified: Tue, 20 May 2025 22:08:44 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json
