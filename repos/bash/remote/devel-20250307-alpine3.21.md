## `bash:devel-20250307-alpine3.21`

```console
$ docker pull bash@sha256:1119a41f03a99199ef18226a9e0a49400e6202b8b57d721560831fec8f79ee6c
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

### `bash:devel-20250307-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:3c6aa49755c4f4801b757d154d7444dd575e5b58afb8ecceed61f52dd6852eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6599734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6417542ad283a47b9c09b5d2f423e7a0d7871a082e65b777d3d7a9c1f721f3f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509e6194e9c4270d96bd1932f2b4412a012ea502f55faebe612462667faf8bf0`  
		Last Modified: Tue, 11 Mar 2025 20:48:18 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413a84ce68ea5d94cd9330ad893a45f13cb2748457c94ed1683a560b257dab70`  
		Last Modified: Tue, 11 Mar 2025 20:48:19 GMT  
		Size: 3.0 MB (2956696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6b8a96958489d16b015c0afaa69a8fd12c23618bccbdf767b92944b2894145`  
		Last Modified: Tue, 11 Mar 2025 20:48:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:74ef2d05b8d7e6d3f5e9cd67c3a496f6fa07213686f9486df9c30704b0e72cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca1e9f4ff4c7b0d598dbe11aa58e1756a3261855c62a2cb9c1cea4afb7b34fcc`

```dockerfile
```

-	Layers:
	-	`sha256:1afefb22a3333ff097369c8e29ba55fe3d6cee9d2347eaf8bb2c609de3490772`  
		Last Modified: Tue, 11 Mar 2025 20:48:18 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81f92eec0dc7d8362456a732381e00f22070996793206ef2f81b51f654413f9`  
		Last Modified: Tue, 11 Mar 2025 20:48:18 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:2a315b9754f34e6464068554ce4da2bfee42ee58f0774ea8d95f70d2d0b462a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6258135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88ba0835f2d303aa0ead28d93fd5e6adb5eba4c929ec7608bfbe8f5a10c8f49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
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
	-	`sha256:0be435f28f20a52a02b7df14e33f42c28968c491f6a2b11532c441c99ced8eca`  
		Last Modified: Tue, 11 Mar 2025 20:48:16 GMT  
		Size: 2.9 MB (2892608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be983c077379fae4ba36e317d4d94e053b6c725107b0bf726315957e82c8d74`  
		Last Modified: Tue, 11 Mar 2025 20:48:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:43f1b1602252d93746ca77423a6ef1452a6207df02f50c6164a84b2712caa5d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87369b1187e413176d35b87388c206c3b1b87dfe9c710e3bb75a0178522c9504`

```dockerfile
```

-	Layers:
	-	`sha256:981ffd9467c918a23b9488628cdd490bd2e47349aefd72839b58963019009ea1`  
		Last Modified: Tue, 11 Mar 2025 20:48:15 GMT  
		Size: 17.6 KB (17570 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:11dbf6c30136294244a33a539522eef4ef9411cc7d93c3e0e95fe6fab506f22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4677141d558e0831ada733af2de5d4d943111251f143db0887dd8babbb2a9246`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b56ee31f8c29fae55a5fb3c5d7c4a2dab0e0ba6d7478f378924f1e68ed88b4`  
		Last Modified: Tue, 11 Mar 2025 20:48:12 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3834be85165c23560e8dad934166dbc724d626a9e32799fb5beb8c0f5808e8`  
		Last Modified: Tue, 11 Mar 2025 20:48:13 GMT  
		Size: 2.8 MB (2845275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc49930e7df2b279bb191918f541ec301a1d99a6b4a30ee49d524f9ce0b174`  
		Last Modified: Tue, 11 Mar 2025 20:48:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:8e34e5277cd250def524543873047467ee48a7ccc2d7dff6f9c6df0d1a666966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f51e44318f3cd1c33c7319768bd2a7f097ba058e8e5dbcef700b1c1a6ee484`

```dockerfile
```

-	Layers:
	-	`sha256:a2b9b9499e529d4754b3989a5701c685293b0bcc665c72644ea3082e99991390`  
		Last Modified: Tue, 11 Mar 2025 20:48:13 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd15dadf8670caee32718bfd5c7f9bc2dc4ff9601b23d802dcbec26a7fc7af5`  
		Last Modified: Tue, 11 Mar 2025 20:48:12 GMT  
		Size: 17.8 KB (17785 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:a3e998d6c7df49fe6c9a741518e09864c61249df0c41d58f311d3f41bdf42a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7037377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86603e193b6fe0a3beea437c7df83c7c25e6155f3b4421c31d1eeb88820b7d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4977a699fe507c4e7687ad9af2945aff897442ecd59a622a9b94afb35bb87488`  
		Last Modified: Tue, 11 Mar 2025 20:48:38 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d4542a01e49f8ec19e67ce5a361ff45d5d8d58b2a2a3cac44fd4ea81f5d9c0`  
		Last Modified: Tue, 11 Mar 2025 20:48:39 GMT  
		Size: 3.0 MB (3043557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca37e92e46f9a371500a5d001383b2b05a7b9e4de570f128a51e761ff1b018d`  
		Last Modified: Tue, 11 Mar 2025 20:48:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:3e9fe6ef24c61fb71de97426d8e8fe7aa2bcc933229a3c75c7196cf9a9648316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4957f8ebf0513f9e732cbb295824509872a1388d44971f9473924a271f729fa5`

```dockerfile
```

-	Layers:
	-	`sha256:f875977e57e643cc2d5b513c6ce6749ca97d16d7215e8e04cf239ebd6f7e4fde`  
		Last Modified: Tue, 11 Mar 2025 20:48:38 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e55cf478111347c35c16c04130ac23b1b28b230705374ed11190dec8b82af2d8`  
		Last Modified: Tue, 11 Mar 2025 20:48:38 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:520c91567e4676bae0aeab75379d313f1124436dd1ae3bed67ac8164424b52ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6348410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc534f6ef2cf84c9befcf5e063bf3b74cce45b9d701ea285b0e06c4499bc1fd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab9bdc0ac021ca319ee583c276b80343abd9d924550b23b4b1314464751195`  
		Last Modified: Tue, 11 Mar 2025 20:48:21 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8064ead3324cfded4e0316a1766254b40f4f36fda237008ce2b7f77c0c7b0649`  
		Last Modified: Tue, 11 Mar 2025 20:48:21 GMT  
		Size: 2.9 MB (2883994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2857bea3cf0c552fa82cb85b3d0ebecf1ddc82b73e73db5ec7187cfd92c4bd9`  
		Last Modified: Tue, 11 Mar 2025 20:48:21 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:923eb7a862df226dea1d2dbb31e97ada8d7f1caee8ea36c846985033d6eeec24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a701b095e11448666bf54f43c004e91dc81b72bb7d332f979b9ee6fbab629c2`

```dockerfile
```

-	Layers:
	-	`sha256:f67191dd7efab25dd0e7f95b7556a785bc883a3d9cabae307f711009ea92a62f`  
		Last Modified: Tue, 11 Mar 2025 20:48:21 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a4ea6e45f9a96be104d7b38eee26035713323f04e01ad97c8e6bcc909d2964`  
		Last Modified: Tue, 11 Mar 2025 20:48:21 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:5ce1a03637f4e9bc7f231586fd2320a305196995ec3527b3289b17e92b4a2083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12143bfbf2eb41934cf858aa686943fbaa7978594dd2303c1f33f821730b0146`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1280f4f21025c8a8249b961886a7780e4ded4b1ce090628e079bd399c5d68a1`  
		Last Modified: Tue, 11 Mar 2025 20:49:03 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3075e0fc660a275fa501c97689aa771450c6dc30b007de86dfd0a3d239d5bcf1`  
		Last Modified: Tue, 11 Mar 2025 20:49:04 GMT  
		Size: 3.2 MB (3228399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48217bbaa9e631f8842483baacff05a91d3aab8c088eb5423b4d6d836388a03`  
		Last Modified: Tue, 11 Mar 2025 20:49:03 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e06b579a8911334944bc7771aea6fb279c17bf3150c30da3ee71e5db8f816f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d38f65a8d62ccb4dee2cd01b26de38e2b3a0f5fb876f52a0fa2cfa09f4f201ee`

```dockerfile
```

-	Layers:
	-	`sha256:1abfefe9dbd97e8dedc7e106f05cff3e00155c910e8d39c8c277fdaa09f10eaf`  
		Last Modified: Tue, 11 Mar 2025 20:49:03 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45531d89173efd203158035232191c74f17d6d222351d6a2610766f7d2f0ffdb`  
		Last Modified: Tue, 11 Mar 2025 20:49:03 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:082978d207aa53c187b65235860c89905cac143b8ceb25b401b4206b566aac0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac44889aa186b3b1e3b31fc4d0e908e52c21f34f5318865888f3bfcd99f08f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
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
	-	`sha256:14b86ede6ef066f2cff3b4521d493bb373486c21465093565150e343e9ef11a7`  
		Last Modified: Tue, 11 Mar 2025 22:20:49 GMT  
		Size: 2.9 MB (2907213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce78bbb6c95b378ee5751f34866a8a9927860add1c22eba2c3dd817d3f1808`  
		Last Modified: Tue, 11 Mar 2025 22:20:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:6c3d692d0c7d8b634df15226d1f4cca8c0889b0f9762f666305f95d1ae4dfeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d1cd0dff4db45ffe99f57b586c0029b8ef0bd6219f090fd92da6dbdde0f76`

```dockerfile
```

-	Layers:
	-	`sha256:1b66e9d4236b155dc575ba7ac3bed18d04577e563bfed00d1409295a8d39d4b2`  
		Last Modified: Tue, 11 Mar 2025 22:20:49 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3940985237115a92c09912c68db91967a3e9d4ecfbca6bbe2ae4984be904c5`  
		Last Modified: Tue, 11 Mar 2025 22:20:49 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250307-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:ec2e249eb98c48e2a53da0af27956ec5f2e5119dcf9f386b74a9a6ec5fdfc9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6521931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc48ab3a9108bdf58aaaece37969d8f8de67926fc6e052f340f90803d38f22d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_COMMIT=c3997d51f8ba359eeabb45b90b9cdae4fe599b5a
# Tue, 11 Mar 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250307
# Tue, 11 Mar 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Mar 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Mar 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f4ac39b5f51b9f9252bd39cf25174d8b76968b782e4baf8aa5b650f7155b9a`  
		Last Modified: Tue, 11 Mar 2025 20:50:36 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3076535e1af60a1def58a4675877e6a0571015cc673b42b386132d39a5c30e`  
		Last Modified: Tue, 11 Mar 2025 20:50:36 GMT  
		Size: 3.1 MB (3053570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740f483db3150d1a0eea66273cf76e04fb353717b64ad16444efde747e6c498c`  
		Last Modified: Tue, 11 Mar 2025 20:50:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250307-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:726b8abbb945d53dfe732d7712f6068f1ecae7b1c64bd0d065e7c43fd2d51318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3ef21bcca26bd39abf3665aea0d6c815755d097980fc970a3d332e2a4a6622`

```dockerfile
```

-	Layers:
	-	`sha256:7155995746f99e1798dd84c21f37356381064b0fabd00ee64fe77969cc166de0`  
		Last Modified: Tue, 11 Mar 2025 20:50:36 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06da7cec2578c10972f305fd2b81e7df871cf718f1df0823c5af086f8b3d8380`  
		Last Modified: Tue, 11 Mar 2025 20:50:36 GMT  
		Size: 17.7 KB (17708 bytes)  
		MIME: application/vnd.in-toto+json
