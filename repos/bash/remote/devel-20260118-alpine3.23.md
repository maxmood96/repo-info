## `bash:devel-20260118-alpine3.23`

```console
$ docker pull bash@sha256:511bac021a54a450b32357449eac73afcbcef482cac54bdf2d019724815df0e4
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

### `bash:devel-20260118-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:20e8ce4917f5ee31bf5b1c4585cf07f38a9f21d12ce5bf83f28f320f2f0e889e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6878633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa736e4c461abb8133f685ea9af80aa944969f660f94470ad611f91e023398c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:46 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:14:46 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:14:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:15:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:15:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:15:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:15:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806639892e9f9100d41460c096df430b3b92c3d4c25a45a4060da75d467edf64`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 453.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342fe1c1ad82a80b8972d419477d00ce7c45e4d609828fdfef7edfbb03aa8df8`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 3.0 MB (3016028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3294650964693701c2b215b2a0b4c07beb4aa38d6650a3f15dab1c83c93594`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:ce8ee560ce36ddaeace4fecc16f1ae2c429326932a37fbc0e6ea5c9c76e29624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (135018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb7409722b5e5c668fff448e984fd2269e685b6e82e8e7ceaf7d19400db3622`

```dockerfile
```

-	Layers:
	-	`sha256:83b2b4feeeac0e6d015431f76d905fed6d89db9b1dd2e4100c0b6ca1b85f0907`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a6d649edbdfebb16b8db0ffb885242227421bbe7020220839edb8ec34b9237`  
		Last Modified: Wed, 28 Jan 2026 02:15:31 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:70b604ffd34ed798c35b8b1e992c94715d327ef65a5a12f1567084d3a1bc5a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6544277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273bfe43b2db046351dbf7c0dd91aa4c8c94d7a158d5b44226d9754b7ad675b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:13:46 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:13:46 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:13:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:14:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:14:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:14:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d51c41aade08674488b3d26e51f52f6c5309666e9d606fc42089d2bc7c97f2d`  
		Last Modified: Wed, 28 Jan 2026 02:14:34 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ad7be54f01366e4072a126defc9f97e8520ab4f7d54b2fc7966a3b3d034b14`  
		Last Modified: Wed, 28 Jan 2026 02:14:34 GMT  
		Size: 3.0 MB (2973668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05cc0cc5b88a420a326dba40e5ddad09d720a238ca2a90c8c35b54cef9f9a65`  
		Last Modified: Wed, 28 Jan 2026 02:14:34 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:5f52c809414c076825859e35e70a18b711e393d0c198a4808c70d3d17647dbd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09eaa220d3bbf650e6ac040b3c946fe6b2f64a28a0b46f87952d44c1627e0b4f`

```dockerfile
```

-	Layers:
	-	`sha256:84ca8106df2c4b7cfe3580acf9fe681063c5b951c0a2f11b6f7e3466719a53f0`  
		Last Modified: Wed, 28 Jan 2026 02:14:34 GMT  
		Size: 17.8 KB (17761 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:8c82273df06a8498ca0f7adcad0ace205eb9e94457167c413ec71b218425e9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf7daf13abfbd2f65c2edcf4aa620d5401be0bdc40e6990cf0aa4fdc187f50c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:13:46 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:13:46 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:13:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:14:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:14:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:14:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa90108b595d6f7c58a90a9c10116c40ed8681800d4431df6fca22e1d0337df`  
		Last Modified: Wed, 28 Jan 2026 02:14:36 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14230e186b919a042d7de7d4851be8937225b483447fef56f0d9f5c2eccfd7de`  
		Last Modified: Wed, 28 Jan 2026 02:14:37 GMT  
		Size: 2.9 MB (2924299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf16662fa3afae10f4548200111fd46dd42f577ac727610cf95f6046ab2bbc2`  
		Last Modified: Wed, 28 Jan 2026 02:14:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:8d49e19dfb3d5f75491b345b7c56b81ae1806da97962d3de73ce0f41b6ca63af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7390b9a8dea068158d0dc8368f951c33f80ecff235ce4d7656280cba7b92f8b`

```dockerfile
```

-	Layers:
	-	`sha256:caed75fc8a7204f407df72ff0a5034373a4d8ee123f4f8f45529ac4767d26370`  
		Last Modified: Wed, 28 Jan 2026 02:14:36 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6d285c67c8aa54f27b7bb5c1eaa17219ab0ecb09d142a04d1bdf887c40a8b0`  
		Last Modified: Wed, 28 Jan 2026 02:14:36 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:dfd08aae7d62d96ec1e3d1a1f6e21e8c4f938e60b8ba9ff7a6a65136fd6ab4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7280694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:038fff947d62d4297db54396a05331a259f8725c8dbc2557faefcdd3a0c7b331`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:46 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:12:46 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:12:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:13:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:13:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:13:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:13:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b479323ad42a9c88f2f0751fdb6efccf9093457cb6de786fb363c7cdd800ce`  
		Last Modified: Wed, 28 Jan 2026 02:13:33 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca3998f7a4f07169459126bf22665f5e66d9c1a0fca21fbfaf48a39d4663013`  
		Last Modified: Wed, 28 Jan 2026 02:13:33 GMT  
		Size: 3.1 MB (3082817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d7a0f5f1e80b9806a362103cb66c888eea8ee7aa78443a205a2d4dd1a3905d`  
		Last Modified: Wed, 28 Jan 2026 02:13:32 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:6c87ae2919bb1af0c822d17e541338e041bde09e25b7eeb24d8fbc8df3b081a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c139a070a46b1080239a6d85a16e15769257d31a295123af95b7104786e9ef53`

```dockerfile
```

-	Layers:
	-	`sha256:bfda81258cc836599e648c80f63d68e5a8620e1ea79c981529b4e723684c9868`  
		Last Modified: Wed, 28 Jan 2026 02:13:33 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3969335a7ae38cc46ed2f4cd607c52df25ed35c61c05cc5c233bb5b5e458ba24`  
		Last Modified: Wed, 28 Jan 2026 02:13:33 GMT  
		Size: 18.0 KB (18000 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:af962dfac852ad887989cf6bf0dd6ade4e55d7d25031a35e75bcaf1f7f707662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6630566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f9878ddccfd9236e84a30062daf96032c1caff10fbbac2862e72ec64602ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:14:17 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:14:17 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:14:17 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:14:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:14:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:14:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:14:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a265c2bc750a16f6790e326d9b86e9489c900be36b794167691293e1da8d41`  
		Last Modified: Wed, 28 Jan 2026 02:15:00 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac4620aa2a9806e42e5086010eb2e26b90f1dce90a7dc3d3eabdf97192978d0`  
		Last Modified: Wed, 28 Jan 2026 02:15:00 GMT  
		Size: 2.9 MB (2942780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacef458f01fddbb6111a10d559b546be4b441212ce6911ab8f621e4aa7dbb4d`  
		Last Modified: Wed, 28 Jan 2026 02:15:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:05889ec38a235843f2c8d6d9ba89c5397414c2f5002a39424928bfe005c1ba5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (134960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762d00df998770527e65b7684d0d941ab5d8a6bcbafb35e473b1aaa81a662be7`

```dockerfile
```

-	Layers:
	-	`sha256:63dc9f9a409fcec56ae50467425050cee84144b65b37eb7b23765da45723f2f0`  
		Last Modified: Wed, 28 Jan 2026 02:15:00 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386ece2e4c054a89534f0c6096b27dc4d557f3255e7ed6bf671885a8e261ce11`  
		Last Modified: Wed, 28 Jan 2026 02:15:00 GMT  
		Size: 17.9 KB (17863 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:0321b1bb61e78f0ca25f2a81473530f0748cdd3fa7774f788551f9191511814a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7151474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dfa773e4fb02027537b0d74f81bff4129e2b2248124ae9d9036889badb57c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:12:14 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:12:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:13:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:13:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:13:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:13:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1df562137f442ce368a20fd090a2aee8c61c51133b0500c9b70a1c208a23adb`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2efabdc0eac0b0fb58789a05e76ae67d765a4668fc800ba82160f7e7a64bb8`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 3.3 MB (3321038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d3d9fc8e91b76108a64940a77b745ec35bdf0a5e978e9775ebe21579f86aaf`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:d7f7bb0685a4f007b7c9e585192e8617b05778ac335fdb62b0e7dca8eebdc23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259fb9c9da5a15953d3beee83cde46f79fe785f7ea11382e537c0d900075c723`

```dockerfile
```

-	Layers:
	-	`sha256:1b475c4bc6e702f9a6c5b9c7d6739ad429c8b151037f8b81d59311de559ca81a`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:520462fa175bebdb7ee697d952fa78a6b42b883fe2621488691d5465ac5f42c7`  
		Last Modified: Wed, 28 Jan 2026 02:13:20 GMT  
		Size: 17.9 KB (17940 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:269c06ce4bf31eb706e137c78c0ab9c1e1aa44c5bf0403ba32d7917aaba3f2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6790936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b228779b20be6c8859b17e797815d0b5438d2a2a5cd44d796b1b0327c253d4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 04:17:11 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 04:17:11 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 04:26:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 04:26:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 04:26:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 04:26:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0540f5e7cbbd06be9591105e336b004c6e351dc53f24f7df485f56578662b1b4`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc691d6b9fbf13713dcf082764ea2ca8cfa0dd4f6521c6684b3aa685305a1ed`  
		Last Modified: Wed, 28 Jan 2026 04:26:39 GMT  
		Size: 3.2 MB (3204851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d92965ae2ae3f5a45ec09984ba79e70fc3e2c4316239e82ab91e117a9c5d00`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:4ff4d2d563b36659d59dd6730090613180d780a5254e84117f74f626d4d37ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3033d5d70c9796a6b49a2df3d6ccf0d0756fe0514a7bd5d1dd72f5a792db4820`

```dockerfile
```

-	Layers:
	-	`sha256:749dd99a8c04410b852737b018cadea59a901c7d59e1c67467f91cf2993768b2`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09ccfc8aead8741513145cf572ed0ce530eb3775fb047c9411bdf165f8df41b3`  
		Last Modified: Wed, 28 Jan 2026 04:26:38 GMT  
		Size: 17.9 KB (17940 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260118-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:cb9c4b3737b2214a89653559a60c05517cd07bda0f8c73a6b9dfa51238a14bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6833678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a757c3a9770dda3fe6e9cbcf00cd76ff8a540647dea503babfdb2154adcc1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_COMMIT=c4b56ed9ac00424bde0f9ce3adfb7edb3d19a557
# Wed, 28 Jan 2026 02:12:15 GMT
ENV _BASH_VERSION=devel-20260118
# Wed, 28 Jan 2026 02:12:15 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 28 Jan 2026 02:12:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 28 Jan 2026 02:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 02:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Jan 2026 02:12:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933f34932483ae323b9c0468361629e1e26fb7403cef6d4353f0f81140eed823`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72f2360a41a4fa6e0dd95b1e5aaa6cf49a54e572eb17ec19b6988ea7f45c062`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 3.1 MB (3107553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabc1d89a3af12dfe8436c0196666dca645bf5ec6fd93229afdfa711642e5912`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260118-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:16de9448fa5aae9957b458c5b469965c93254609214d6ea13c85a65ef50ea78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1915d3b22b4c55b370ea2b825ec237f8ea5791fefc3916ee31c38b0a534c0d`

```dockerfile
```

-	Layers:
	-	`sha256:1228b4387a857af6f643d32cc147cc9dd65007f281a689436b031ca04c30245c`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05be319e3f5a7118502d7ae36685827a9501be474f056905699e83db4a7493b9`  
		Last Modified: Wed, 28 Jan 2026 02:13:04 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json
