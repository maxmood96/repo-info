## `bash:devel-20250324-alpine3.21`

```console
$ docker pull bash@sha256:d1a8d3918577878cebd54036e173a672d08114fce9a9b6ef79b80af765687f1e
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

### `bash:devel-20250324-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:ddc17253caa564aa08b0fd0ed0b575f8b8ad1d3b19c4d67a7d8f200af7e27c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b71d1b048a28c21c1c2914422b0a4959c4010643b8ec124207beccd2b5347d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef84928b701c19f7a32f6d5890081a34f877ffd7df99bd3ecf8c4144b085c6e`  
		Last Modified: Tue, 25 Mar 2025 20:47:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24451c3f14b417fe21dc7fd0ed02ba21930d214e1721342f3ff51d2ddcda7c8`  
		Last Modified: Tue, 25 Mar 2025 20:47:42 GMT  
		Size: 3.0 MB (2958388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aae6fef2ca8f886540f5e54a65b310a1f819c41d82eeed6eac633e0c4434da`  
		Last Modified: Tue, 25 Mar 2025 20:47:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:47c3ff52942df61513dcf1f0b011f1ea264155d9af08f66237047c4a68a007bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c20f9eac9a3eec964e684f1016bc22b40806a134eb3994a34ee2b15c523b49b`

```dockerfile
```

-	Layers:
	-	`sha256:8f5aa4c21ae05ffc690c88feaf9323b2f45c494cf110241b923489f15da56603`  
		Last Modified: Tue, 25 Mar 2025 20:47:41 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1871f55ff9e864506de5054d26fdb41ef4fbf01ea7a1d31019c41b964a7bb7de`  
		Last Modified: Tue, 25 Mar 2025 20:47:41 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:12a2ee237c9a031adf008cb7d2563cad580ba71a6462399a2dbb9bfffaeb5368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516cf310f78e1447e5a4a5fd852ecc83c51dffbcb8c8b3554b2faee2e14e3832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
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
	-	`sha256:71aa560cc1772a5af62043916677bf0cee1cab0ca2a10b56d0340e62b43034c9`  
		Last Modified: Tue, 25 Mar 2025 20:46:38 GMT  
		Size: 2.9 MB (2894229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c290232aaa59e53467a174b0d52556ab278cb7b48f2c47097c0c17959ffae93f`  
		Last Modified: Tue, 25 Mar 2025 20:46:38 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c755023c61ffe0fb10c3f006680988f7626543612a41f7bbe056497fd7e72640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ea9bf5a0fb8b61ece5942f43825477a274850484d089f9bc6996a7de630af`

```dockerfile
```

-	Layers:
	-	`sha256:402b96a5cc92efb69b1a240f3653f91b86d3e1506742511ca9f4bfd6a92996a9`  
		Last Modified: Tue, 25 Mar 2025 20:46:38 GMT  
		Size: 17.6 KB (17569 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:001dc83263c640fd57f431f70869af1c1faea2c179efb3bc09c58b4e0587dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72229418cc1d49195db32cb5f4cedc76d092169b17d6cb9be4aa01004689f0ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
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
	-	`sha256:194b15e44bb43e010d2ebc91c6d710a63834f5072abe1a5c29fcef61e932a831`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 2.8 MB (2847149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e200907ac59316d6fba90f37cff203a1699e16ce4ee22212e9e97929cf8126`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:ef5012815275d68bc4c98dfd7f32577fe3baa94e1e45c7e9263191e6c9e97dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fe20b12070deff1c06b0a33c22e7cdae6c1f8293a9a3c1637c6af1d763b2ff`

```dockerfile
```

-	Layers:
	-	`sha256:ba7fbf4707584c3a1d7ac207723ad578007dd176ac037b62f9e6b148a2dd58dd`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1239b5e6bbbd2f3d5cab6f5e3e5e5d6caa1736a26dd1f86a7b8c91da6b22da8d`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 17.8 KB (17785 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b8e58a46e9c28cd9c15361f74862283410fd7970807c77c6251efc57f8576848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4345300303988b602383f6fc9281e0642abf1e0f44b5b337d000cf58db6bff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27160156f03a0dfb7ef4c6d04f3b71460108c15820b401635d649316089fa1`  
		Last Modified: Tue, 25 Mar 2025 20:46:39 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af54365851bfbf66217c8568ee90482abc9b267d4c476852634922b78cfa933d`  
		Last Modified: Tue, 25 Mar 2025 20:46:39 GMT  
		Size: 3.0 MB (3045421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdec2d8298cb0bfcc1aeb3200389c0a37a32d0d6b7bab6abd2c08f86ae7390`  
		Last Modified: Tue, 25 Mar 2025 20:46:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:9ef0443dcbfe090c90c81c1fbf529e4cb08f1168ae34759c3b0e97f5545ac5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85969f7ca0acd50c953abdebad6b5f30b04fa0253812ef307a73a9652a9293e0`

```dockerfile
```

-	Layers:
	-	`sha256:7c06d9a24e4718375e7d805ba86ec3244d16a6b4e5c55ed1cf908cd115810fce`  
		Last Modified: Tue, 25 Mar 2025 20:46:39 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:710b161f4db51ec4c813309ce89bd6bc4c3fe3a6b6f8bf214ee69547614d4c52`  
		Last Modified: Tue, 25 Mar 2025 20:46:39 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:e19623f86ccd49d9318f6ff6ade33b9a85c60d1998ba54f57f00a9b4af83ca6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6349990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56078ffd7a077da303c24fcc140e9dad0a06a273158e388b6bce906e8c1afc42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6b12e3018e9e6e52ccb04734bb504890351f76d41574045c1b59b3673ce72`  
		Last Modified: Tue, 25 Mar 2025 20:47:09 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba5144360c51004ccd3c8e0946c0ad9e214723f91c700e0b8ee957c79906c36`  
		Last Modified: Tue, 25 Mar 2025 20:47:09 GMT  
		Size: 2.9 MB (2885574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fbd5eed6773bf113de817fb2b6ca269f453ced88c9660b83fc6215227f3c1d`  
		Last Modified: Tue, 25 Mar 2025 20:47:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e6a03533261978457fca0c1f31b4d26f8d793abe1fcf301738182f074808a039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19589cacd7c5acee6158bbba709078effae51494172212af85d2c550e1a85e56`

```dockerfile
```

-	Layers:
	-	`sha256:778ec90b21581ba2e31c6eb1d0c004163b6092ab5304ab0603168cf14e5d1023`  
		Last Modified: Tue, 25 Mar 2025 20:47:09 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2394c9d1117f78a72413b44e06bf7e77327f6831053cde67ac8885f20dfd0ffe`  
		Last Modified: Tue, 25 Mar 2025 20:47:09 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:ce0a9b615ad9cb6c1552508a3dbe9f7a8f420fccf60c5009d7994c788f63cb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6805574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662785c734e5b451b36bb8e6c1ebcdf36204bb29fc06ad144bdd6fcba682e2a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9475e9bda4bf8d1c878a530e2c8704ddeb1b8b48f05ff96c448f622f044fdd0`  
		Last Modified: Tue, 25 Mar 2025 20:46:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0f6f2f7dd86a848bee68fdfa40047765876135015845f7c93bb88a8d14c32`  
		Last Modified: Tue, 25 Mar 2025 20:46:53 GMT  
		Size: 3.2 MB (3230435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d8d9d660d598eb49a4d22e59e0b018af9fa957decab971bd6d804958444b33`  
		Last Modified: Tue, 25 Mar 2025 20:46:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:247e88ae6eff6c9d7cd91bfd7c1278f49c768e5e5691dcead0c9e8e37a30e823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dc24a712945bf7fc04b362de8d7d3991ef510b4c67bed7596b441935a61f37`

```dockerfile
```

-	Layers:
	-	`sha256:03e238429c426fac37a4ba5ec9d1efc1fd8a8de0963f279365af523a37d6f6cd`  
		Last Modified: Tue, 25 Mar 2025 20:46:52 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ded88871e3ec505640e1b0b167e66a4efad6a9d54671e3f8bd797f90cadf9a0`  
		Last Modified: Tue, 25 Mar 2025 20:46:52 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250324-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:2b6bf6383e7ec8b4ef99e75db63ca6e06f6f46c2fdc6b47ca2e8d5bf2bbab806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6523925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987777c845ad7943d147ebb07af669844f18902d39e4a918e49795680317e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_COMMIT=e009d30dfff92d5389f7bb05ec8627e524d5a0ca
# Tue, 25 Mar 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250324
# Tue, 25 Mar 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Mar 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Mar 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938fac8358e6a698a64c69e9876d1469da804cdb09bb1fbc7cd7f4466de7e7fd`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfb36140a145404e4c394b88b103045491e28e7a91f96d694f79d721f772f55`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 3.1 MB (3055569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025463c82a1170123f3da04dbba003d1d6b9501b80ef63f5ea0c00a155b5c66b`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250324-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:02cb4e87ae4a027cec80fcc42149d8f96c6e7ab9d0c7722eea16d894270c8a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7026d835a4434cb160afbd44029b82df581c68443cb0a7d7a82c58c522e1f39a`

```dockerfile
```

-	Layers:
	-	`sha256:20bce742e102d6ad29e03a43d8fbe1ebb2fa683440b662a043a9bdd90a7d37fd`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a14bfe184d8a7f7154adcf879c99e4b51020bfa94cefd63d790e97613a2d0c8`  
		Last Modified: Tue, 25 Mar 2025 20:47:22 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json
