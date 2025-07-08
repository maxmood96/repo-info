## `bash:devel-alpine3.22`

```console
$ docker pull bash@sha256:83f99dccc485a17207a8e48cda195218799905deb338636992d895ba24382627
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

### `bash:devel-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:3ed69a58428cf1120aa35aea6dd7380a2d6a90fcf54fa880323d8cc11547c090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad3a2e2b1e65831cacf642f9a6b8a6a131b684bd2d6f81545008d1545bd37e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2cfc17b65ac62faa6d53138bdf9d0e9a9b3307c6ca76823fc8d1ac1050e29d`  
		Last Modified: Mon, 07 Jul 2025 22:56:47 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b58bbbb3b26b1965fd5fcf8decb76ae9337e26c6d93de75406d2504a3b0672`  
		Last Modified: Mon, 07 Jul 2025 22:56:48 GMT  
		Size: 3.0 MB (2998334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74270d511227ae798071e909190a43e406fe310b125df08f378711eb1fde721b`  
		Last Modified: Mon, 07 Jul 2025 22:56:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:99837adbc2a96536f156a3a5873adca09dad2d9686dac1739b0ca165e458adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 KB (136364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e32c92b03fc857929d8da8190c22039f2813813789e35db7315c7b0b9a4c5d`

```dockerfile
```

-	Layers:
	-	`sha256:9a848395ded2a94ff6b16930cb8c301d3e259f6afc4b4c479d956326b4aff34a`  
		Last Modified: Tue, 08 Jul 2025 00:04:04 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6d2153e36b6caf042e5fe247b25b5dc895aa4982db2c64d3da9f6d85b84990`  
		Last Modified: Tue, 08 Jul 2025 00:04:04 GMT  
		Size: 17.9 KB (17935 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:685e538cf959a94eadf661e950b08fe035b079c0bfcd802fc7153445aa4f1422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718d7f1dbefaba17540a4dc0218b69c43e738d9ffb9e6276556411345bb2b73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa72c6a9e21dc757e636874754288c8a9e0c46684f2567c68530f8619b60f607`  
		Last Modified: Tue, 03 Jun 2025 22:50:33 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46707a13baf70d2d43b14f85ea191439e015cf64c9cb80947a5b8d0130d37b22`  
		Last Modified: Tue, 08 Jul 2025 01:00:51 GMT  
		Size: 2.9 MB (2934397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5b5bb1ceb844dedf068c7d60613cfc3ec6b8613b035165f0572c7c56a5de0e`  
		Last Modified: Tue, 08 Jul 2025 01:00:50 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:fdba445a63a2decce23c75d5cd506367b2dad4b4955dcf9d6dec4c2d434ad6f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a515008eb66d1e21faee057d2618a0d8a9b0272ba18f41ea9dc8f26952029138`

```dockerfile
```

-	Layers:
	-	`sha256:d65d9d134ddc2e48af89817e8aa271e4bfd8b548c4d9799cffa79dd66b99d86c`  
		Last Modified: Tue, 08 Jul 2025 03:04:32 GMT  
		Size: 17.8 KB (17795 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:a611f940f989b886ccca5b8c2f35c03371c80c110af54025d2a9b1dfc1c1ac50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6105066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c759d92c5c6762bb31d2c323806dd2bb151e23397a7db9b870a6873f974dec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db02dbbe1f74b9e1a4382164d56b37b9d34b5e372587e81a7ce31869407df07`  
		Last Modified: Tue, 08 Jul 2025 02:44:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd9608567614dc47640914d57ec5c90c60c08704060033cd47bd841e76a2b19`  
		Last Modified: Tue, 08 Jul 2025 02:44:52 GMT  
		Size: 2.9 MB (2885093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953c4163ec2eccc3461294a96e4011b34ff5dec51fdd4dcf86bb7c0388e67b1c`  
		Last Modified: Tue, 08 Jul 2025 02:44:52 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:e2ff0e426e5c2e57f2be86dd5b53bc9ecaa0c0fece3e23e714257acb902af90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1c3be4f9fed28372d2e4a520e14030fded29b6ebdae5a65c090506d3134c84`

```dockerfile
```

-	Layers:
	-	`sha256:353c44b4b127d25095d802ec9e8b6fe09384dd7ca451f0c03bf232d131d1b955`  
		Last Modified: Tue, 08 Jul 2025 06:04:31 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ce312c2b4594edd100f990c29265e39b126790b5546bc7d51087fa31af8822`  
		Last Modified: Tue, 08 Jul 2025 06:04:32 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:659757ee71fb80e4c21a8cb9d5a00aaabca6e9c6512b0a5d373e89ea97ed0bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7221570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a19a78e2b088c6bef634dcc5554aac8f6ad60c929a81c17c240080c00fa48b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ab96a3af56128de412effdbc26996ca44b70cf7714b4dd5432e4217cc97756`  
		Last Modified: Tue, 08 Jul 2025 03:37:15 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7084f2be601bfd74bd09327f064dc2e20602a1e41a72627f46cf767186f2e0d`  
		Last Modified: Tue, 08 Jul 2025 03:37:16 GMT  
		Size: 3.1 MB (3084839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21e708165a419a84027b78bc9603ec1f184507abc8a39528c787285278bce8`  
		Last Modified: Tue, 08 Jul 2025 03:37:15 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:ba10b16d5ef8bf51e297ba59ff7f51ba224ffaa87006408af9f944f3b68b8a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf9557e34cef1db0e78e184648504a6562a24540d1fa7b37b9da80c9eeaf97b`

```dockerfile
```

-	Layers:
	-	`sha256:f16840029dd67bdc1a0f46164dc10259fd726b741bc3159b0455d2090e845d77`  
		Last Modified: Tue, 08 Jul 2025 06:04:35 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822ca559e86bceac241913c7fadf83ab8d6b58c6162bc4668f1423c80a58fa09`  
		Last Modified: Tue, 08 Jul 2025 06:04:36 GMT  
		Size: 18.0 KB (18039 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:7c0e373af842bdf066f964b090697c81478267faa9fd7f7c814e79221dc88e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6542006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e4b211fd5d356c22d8d272b179f5cbde04d33c3ee3d5482e3af2ecfe06e2c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f2887a5f1de5c228333b35d13959fbd8ed530628077003652c2f133a9b73a2`  
		Last Modified: Mon, 07 Jul 2025 22:56:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c93d80b9efde93ec8bfaa5d3131119de75c764cd6c7e87fb3e34ff54108ad1`  
		Last Modified: Mon, 07 Jul 2025 22:56:59 GMT  
		Size: 2.9 MB (2925190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2de3697ec3064a39cbe3b1260e755e7988fdb11fc1ce59e556cacdef6abff4`  
		Last Modified: Mon, 07 Jul 2025 22:56:58 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:cd3a0373b04661b2e7e1d2fcd023dd771e75ce277673fe5503de86843bb1828a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 KB (136306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4d4185d5d0a1a56b2ac613a8d3140e0dbdabee3cbe0c2e327c5c12d4441239`

```dockerfile
```

-	Layers:
	-	`sha256:d2cfff15d2812192f77ec016572d44e42aaea1e4aee1d3cd4e1308357ed5a87d`  
		Last Modified: Tue, 08 Jul 2025 00:04:10 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40220c4fce701e570e5dd6879433c27fb7e899346c3a58c38ce16fc174eaaef`  
		Last Modified: Tue, 08 Jul 2025 00:04:11 GMT  
		Size: 17.9 KB (17902 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:18cbbe7d44b1db57fc37d53b2f1648f9d7d9bba34c1cb73b9cae59694f5c36cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a5619de067a88d03e381b61cc5f4b916f89c2066f89c73d171db6c4e6f5fa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89765efffcca1923ae3a7b1e9cf07c0c03dfcc2206e10629bb1f9c205e9f859`  
		Last Modified: Mon, 07 Jul 2025 23:18:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99069664f5f1e3dd6cecf8ef8905c1c5fd3f8ad2ce38b3a877363512d64fee50`  
		Last Modified: Mon, 07 Jul 2025 23:18:11 GMT  
		Size: 3.3 MB (3272718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1626a5c30a1ae61eeb7d3e5f9f03e8ceccbbdfb1bbf0f080e7fda544445a079`  
		Last Modified: Mon, 07 Jul 2025 23:18:09 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:b45ef0b01dbc4c7c9e6d9916ab8371a3d7476d3e6cf25870be2d4dd2428f6ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553bb40812239c670ff19c61e1258e326195c24088aea53abfdb145c8ebd3739`

```dockerfile
```

-	Layers:
	-	`sha256:fd333d3e16177961185b912860b5ca4022cd5f0e13e11623ee306cae6a50adb9`  
		Last Modified: Tue, 08 Jul 2025 03:04:39 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7999b03c29921d5a8dfa6f162e1333018607d8fbacf4ca43d3b768f9a2ea31e`  
		Last Modified: Tue, 08 Jul 2025 03:04:39 GMT  
		Size: 18.0 KB (17979 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:1b52c7f177d57909280a68fdd682116a545672dd11b48ea8bc7a646fdbb1014f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f788bc6a4fc6876fc34ac33c44c38667ec3c7ca90a541d452a7a3a2d4039f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d9c7d21cff81f34ab6ed79c306ac7f740386530ff46f996e5d394f46f4626`  
		Last Modified: Tue, 03 Jun 2025 22:51:48 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89164f5890e45339119b8d80f63dcf51a691bbf291f982f23708f00811c5e16f`  
		Last Modified: Mon, 07 Jul 2025 23:26:05 GMT  
		Size: 2.9 MB (2945222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29ad0780c32e35fcaef1279b209068922ff77198424f99a22cb27caa5f144f`  
		Last Modified: Mon, 07 Jul 2025 23:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:83a97ca9ee76447b5d8192a2152f7e3610938550e69a14a2e511ce6135b90bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbcd5e6396cba7817d16d676351d8a62b368a48566e5390113fc69bb4ea76f2`

```dockerfile
```

-	Layers:
	-	`sha256:f979dba6ba65dc2aea28cd01146ac4d76daf14063b8aa335805363720482a8ed`  
		Last Modified: Tue, 08 Jul 2025 03:04:43 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14277e0b65d33b9b9e52c094b03f068222b3e8279eebe3e2b5d03907246fb8f9`  
		Last Modified: Tue, 08 Jul 2025 03:04:44 GMT  
		Size: 18.0 KB (17979 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:8c77f0c41bbc52fe8337fa1aff1536ce799c7cdf4883a14f2804355c13ea2161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6742348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e54eaf9841f53a150a765c3c21dabe3a1c259d992b465c10a2eb8f6433ab7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e1805ea160bfdc755f4c0717351bae85dcf5fa5d8f24c2281272bd810a089b`  
		Last Modified: Tue, 08 Jul 2025 02:51:52 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c848388c8943e267480465bf05b8b4b72125c7f556ef96198e7441fd46fa9e`  
		Last Modified: Tue, 08 Jul 2025 02:51:57 GMT  
		Size: 3.1 MB (3094028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c49d4da16741eca616f4367ffd4cb2e868b163a2552ea03dee06687dfae4f4`  
		Last Modified: Tue, 08 Jul 2025 02:51:56 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:f85193962d174ea80e9cab6da999d3a07870361d353b20df77efc260ab0d13ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eaf242e6542a3f8eb4e469dfb07efce5e830ee1ab4edf4aef0fc08070cfdeb`

```dockerfile
```

-	Layers:
	-	`sha256:947929ca27894ab53c87e988798a22405f47e359b1032fbd87f797e6ffa41faa`  
		Last Modified: Tue, 08 Jul 2025 06:04:45 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729a2505fbe4b05fa1504f71706493cd970ba3d20faafc73c444b2a53a949eec`  
		Last Modified: Tue, 08 Jul 2025 06:04:46 GMT  
		Size: 17.9 KB (17935 bytes)  
		MIME: application/vnd.in-toto+json
