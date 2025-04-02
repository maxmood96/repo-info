## `bash:devel`

```console
$ docker pull bash@sha256:0460b23f4495568eb90126aadf0866bc0d09ba0fd7f0f6b2ae8e6cd4c4b8d7b9
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
$ docker pull bash@sha256:1c67b41d0010c3bb7a122d56635e94f449668fba2dfcb59b36fee56e01c15580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c310c31675172b8f49f47060d78d22e779bbf36b2a9b6ca4af6e348ef9ee5e1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea7aadd203362e209a44e49151ba04150fbb2c18cc5f93c77da4059255c5b69`  
		Last Modified: Tue, 01 Apr 2025 17:24:04 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3796e8975346ddc3ff8f33a1d8c3f1cee35757e2b36ddc5e6a49821a89a048`  
		Last Modified: Tue, 01 Apr 2025 17:24:04 GMT  
		Size: 3.0 MB (2958583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd314011125f815706b6a0d317665a5c62d98c0b3c10ddeab86dabd4ff8e78`  
		Last Modified: Tue, 01 Apr 2025 17:24:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2af9e5f7ad6582af9c8bd99101a760f56cb81cf66a104f450685706f99792df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c1a6ed11f09b81cb224e6f20fc1a468b04dd038d88785c0f8f7db53407b943`

```dockerfile
```

-	Layers:
	-	`sha256:e221feb4539ea9584f17b6b265a99da3f2b6c4a6e9159f258e5cd8c228b0991b`  
		Last Modified: Tue, 01 Apr 2025 17:24:04 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc65911693c44cc5d0e039b79d9f7d60bfa99568f47eb8f94ebe909aef38749`  
		Last Modified: Tue, 01 Apr 2025 17:24:04 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:fd6e861a87de9838ca3fed39cb89c07ce4ce8a87ff627c1cc175d766cbbe7a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6260239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d3c65baa14e71f769124b64f68f70aa1ee47482bea406522a3399ac2cfff56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:26ed7032d6f8c3397d855279b89c948696df918494218e5f497c86ecf3bda913`  
		Last Modified: Tue, 01 Apr 2025 20:31:40 GMT  
		Size: 2.9 MB (2894714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee4b1bd1310b02ac07a2d03c8999d639fd7afebed1388011d2e861dc6b37ed`  
		Last Modified: Tue, 01 Apr 2025 20:31:40 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d997a7a4f5486328eaae2e24c049fa305dd9812d9838950e869aaadc47378768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b522280e56ceeb2325d415286bdfe44345d8f65e94662152a33c82d85547b9`

```dockerfile
```

-	Layers:
	-	`sha256:e79cb94a89f8163b57cea6e77f5be5b1c556265a3d38e61c21ad710ab1eb352a`  
		Last Modified: Tue, 01 Apr 2025 20:31:40 GMT  
		Size: 17.5 KB (17534 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:ca7f6d98630ac231a707f2d11e0525c86366345171e953650ca3481ee472941f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9ed552e898aa8d7382a6766ea0167d72e87e627d76c827bfe75ebe87c49c67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:c0acd25743d8c5fb057108fb637b1ebfd1e53a70c483f830f8ef5d462c74a844`  
		Last Modified: Tue, 01 Apr 2025 17:35:20 GMT  
		Size: 2.8 MB (2847576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d8b5adfa5c3554961c18008f89dad5d999db1b0275d98445c3d00fcc6bf11`  
		Last Modified: Tue, 01 Apr 2025 17:35:18 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2169a1def96201e29e6d7dace14ddafbe5766936481ad65477fdb8098ed33738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d1270e0616cb1880d051f51661610ea98cd508eb9683a69beec1ab199a550e`

```dockerfile
```

-	Layers:
	-	`sha256:c844bca643d1e8258d8aedc8cbf4934827a8728013ad801a4f03347dab6cf583`  
		Last Modified: Tue, 01 Apr 2025 17:35:18 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778adef7de16b2ab8a7543f828fdaa461f2f70d9477046fe9c0927a96b2e94f7`  
		Last Modified: Tue, 01 Apr 2025 17:35:18 GMT  
		Size: 17.7 KB (17748 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:a2567ac0f0f75dfc220b916c13d4c2ddaac382a625045c65712e866e40c21418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7039975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b217563afd5d1b88addd797226a80e493d5bd974148328e146cb89c40a51a4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:111cd74acf9ed321fa06dea37787bf0386257dfff54f8eee6b17e5891bfbcb95`  
		Last Modified: Tue, 01 Apr 2025 19:37:12 GMT  
		Size: 3.0 MB (3046156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5610e57bc0c66c27f239d639d7e88ccd674c1050915bf7f54a99125c28240b`  
		Last Modified: Tue, 01 Apr 2025 19:37:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0e617f9baa54e45dbe98af1da828f39a62e849887853e41025e24aa1d1ee8519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da4eaec4a583403be391a889d9f39ab9c190d1ebd790adddbb7156d02695a23`

```dockerfile
```

-	Layers:
	-	`sha256:eace4f88b3b3e400f7c6bed2ebbd7277eb79f9934d5ae55089b837f2c7ed57f0`  
		Last Modified: Tue, 01 Apr 2025 19:37:12 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0878b87211823a4f01dd302f1c1224d34dc4c42bf4fbd8d54e1214f09a739544`  
		Last Modified: Tue, 01 Apr 2025 19:37:12 GMT  
		Size: 17.8 KB (17777 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:a935e82b3519980ea4ef366061221e9405c2469cb3f28bb8230a95bb6060eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6350064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f456ec3a1fc20ae5f367d4081976ceaf56ca3b78b7f1d5b8517bd21d1126d05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c594941c5bf4204687d331d14a3bde2913bfb54fc5ce97353bed85e5a0c01ca2`  
		Last Modified: Tue, 01 Apr 2025 17:23:55 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb11afb06c2886c9e79e5ff6da8bd97385ca606b36abcbcc1fb9ef6f455abf`  
		Last Modified: Tue, 01 Apr 2025 17:23:55 GMT  
		Size: 2.9 MB (2885651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c378c43ecd7489fce28e20c284edb6c7ef43e44143d06ef5859b567ff9253a`  
		Last Modified: Tue, 01 Apr 2025 17:23:55 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d483857c2a991112bebc7a81feec94cdcdc601ad4ade4a5f80c66be7b6d0552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc6db058c25d4511930cb31ad1de55ad2432428cd55e884c0004ea2c9348fe5`

```dockerfile
```

-	Layers:
	-	`sha256:afcab0c6721c7803b2764e0acc6e2cbfd9fafa75ac7886a89f7ee13b325c612b`  
		Last Modified: Tue, 01 Apr 2025 17:23:55 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27bc88fbac06565bca704c422597f421a16305895f7da8d4da5d79959f2f6fdc`  
		Last Modified: Tue, 01 Apr 2025 17:23:55 GMT  
		Size: 17.6 KB (17641 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:715294ac3c6d5450344fb938aaf0b472895e479bc6d8848b22565d07b0876fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6805960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb033929978ddb2ce5109e63e29f057cfc8f3408e65b74801fd5fd90053df23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:87d76862ff5c89069544b22f6e1210e1b598d5905fe66028da8d24470046243a`  
		Last Modified: Tue, 01 Apr 2025 17:38:58 GMT  
		Size: 3.2 MB (3230822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb67107e28745e05785add1e31c95650c441f4bab7d3d15fc0c8fb085040babd`  
		Last Modified: Tue, 01 Apr 2025 17:38:58 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3550d31b70e7316e339b15102f24bd92de9ef6981beba1bcbfb9c5b7fb420e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c939d46334123049a39ef0dbe9154e25911913d51b063ab206d6f95049f82a`

```dockerfile
```

-	Layers:
	-	`sha256:473ffd54517b7dff0b28163851cd6dcaefa3c8614646f857c2b8067ae2b20851`  
		Last Modified: Tue, 01 Apr 2025 17:38:58 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d16c5068e898fac0b7b7df56b3b8df94e048c9900190ca125cbee3e6a440531`  
		Last Modified: Tue, 01 Apr 2025 17:38:58 GMT  
		Size: 17.7 KB (17717 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:56977b7ff8decd4e84dc3730f7b0a0152a7068c763e75b77df4d41d0c3aaaa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6261296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12d98a85faa68fc3c33186a2dd71becb03df8ed7b3748f89d824a9da8d52413`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:25e02e27b94a2d5833772e378b7b75a3dff92ea558f33c466a8c06f0b5b88148`  
		Last Modified: Tue, 01 Apr 2025 17:34:30 GMT  
		Size: 2.9 MB (2909063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a5dc692946816016434ad5634b0731300ce6ba382e84bd53967d03707a1b68`  
		Last Modified: Tue, 01 Apr 2025 17:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:842b5f271a176039b263ab84d7799d95b809fd717bfb162c0f3f406f7f48d1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6989cbebe91d51e001a5c278a137d16b5125479275e0ea38ce6f31e42e439e8f`

```dockerfile
```

-	Layers:
	-	`sha256:97e8170c48fa815e573525ed510ef318a0a7327951eb37fb6c5f868583884bc6`  
		Last Modified: Tue, 01 Apr 2025 17:34:29 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3d926943ae316ec7f99964565df69983050b28b18398d410c407b3a6e24c09`  
		Last Modified: Tue, 01 Apr 2025 17:34:29 GMT  
		Size: 17.7 KB (17717 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:cc68d513a9c7a137162f4ccee04f6a5d132f9e77657eb63da134d7fc47eb5414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255c8f94a07e4edde9813f4d18b8032f4d79bb1d79d14759f552af8dd0dd24d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_COMMIT=a6767763de5e7859107711b166a64a9e4a77a8ae
# Tue, 01 Apr 2025 04:18:03 GMT
ENV _BASH_VERSION=devel-20250331
# Tue, 01 Apr 2025 04:18:03 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 04:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 04:18:03 GMT
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
	-	`sha256:3f7bbb53d5d4e1f9e98059dd1bcd3d922cd56befb4c3ea421a9d720ab17019f6`  
		Last Modified: Tue, 01 Apr 2025 17:23:57 GMT  
		Size: 3.1 MB (3055797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74031280862d0c0869177fb7acc8475085dbdb2ca8b101207fde3c78efa8057`  
		Last Modified: Tue, 01 Apr 2025 17:23:57 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b4c64920265e57b4376d43289e744d296673cef93c950303c432ee5ccf8b13a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c7b783b67f09c1153574c0cbaf626198d86d456f83bb8110a0b828db9f2494`

```dockerfile
```

-	Layers:
	-	`sha256:e60e08064adf63e170a32f039d8ff204cade51375ef0e78671fcc7785a72e16d`  
		Last Modified: Tue, 01 Apr 2025 17:23:57 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82400d5eb34c033e0afea53cb13c88f11f1fb8e7663cc3610158dd8cba6f6768`  
		Last Modified: Tue, 01 Apr 2025 17:23:57 GMT  
		Size: 17.7 KB (17673 bytes)  
		MIME: application/vnd.in-toto+json
