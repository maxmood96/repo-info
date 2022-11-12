## `bash:devel`

```console
$ docker pull bash@sha256:6fc3ac7646d07c0c8fee13befb1dfe9ad80d7892daf64739cf13c1e6dd996c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:1169e21c549c557012fdd79d2c22d7d0fa511e774417d7c4ad10a9c28922eec1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9878ea37bbd8187210709aaee1d7620fb0b195fc9e5e14b074ccfa922657600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:45:40 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 04:45:41 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 04:46:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 04:46:26 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:46:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:46:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5aa3cf2f04ae1c4a1490a37ee761db29d89191c09b150dc7250958bbc5353b`  
		Last Modified: Sat, 12 Nov 2022 05:02:57 GMT  
		Size: 2.8 MB (2797861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3595e8347739f9e323ea42155473f09e6d5f9cb44fdc5d151685421d6330ee72`  
		Last Modified: Sat, 12 Nov 2022 05:02:57 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:944ba5ec388077a93e91ecb0183467f8fc5da0bcfb9ec78c3fb9bf918fc38464
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259ad528e47a598425212ff80b1564cf7f298ad62f92d69596cfcad567bc117`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:05:52 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 04:05:52 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 04:06:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 04:06:40 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:06:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce60a947f57a8adaa03a262139186f00063f1e2a8ce1bda8c01f8e153dcbc852`  
		Last Modified: Sat, 12 Nov 2022 04:24:03 GMT  
		Size: 2.7 MB (2714677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53163650f63ae075a9807db6c90255c1948f29c59cf8243fa1fcba501af2093c`  
		Last Modified: Sat, 12 Nov 2022 04:24:02 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:f8eefb95410b1750f6e4ebceb3e9f626ea4afb574c8b9ebaad0d0b6594ad8249
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57488ee2e619168f9f0a921e7a013c7ee1446295c94252032ef000a6bf9b2888`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:13:57 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 04:13:57 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 04:14:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 04:14:45 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 04:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:14:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704697e2baf077f19847baa777a49596978631e9b2dfea49ee649c33423631dc`  
		Last Modified: Sat, 12 Nov 2022 04:31:40 GMT  
		Size: 2.7 MB (2660225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda46180139af634a7a597c8829a5db2b73ea08c6af04dbef5b144a9c77892c`  
		Last Modified: Sat, 12 Nov 2022 04:31:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:22b085922f9edad6c3517dd9a177cc198ae0366fba670b0b8d4cd3ef97a39458
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5503776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1470ffe4ab2927f4a9b5e7305d86ea6a6cc29135550eaf443aa2fb1527bf893`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 03:55:55 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 03:55:55 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 03:56:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 03:56:30 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 03:56:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 03:56:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8f398cdfdde05a2691596775b485be9a927c2aef252a3367ff67a994b445e9`  
		Last Modified: Sat, 12 Nov 2022 04:09:14 GMT  
		Size: 2.8 MB (2795683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14390116944f62a5579e084ab859096caa0e85f86d873cc19250d99272a384ff`  
		Last Modified: Sat, 12 Nov 2022 04:09:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:edcbddd7972a0231eed145ad74d2ce1e4e98ee6719f4efe86972e37f18e04627
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a22c7e568bdedf608c8f6ba49666cf78326aa7f1b93841bcd2c88a3ddc283262`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 03:55:23 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 03:55:24 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 03:56:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 03:56:12 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 03:56:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 03:56:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a63748195d1fd8e6be38fe99be529d23e270ac86821c169587d623096a2601`  
		Last Modified: Sat, 12 Nov 2022 04:14:40 GMT  
		Size: 2.7 MB (2742477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffa27c9901d4aeeddeeff26f69f3b505fac81bf994edde86e72f982c84607d0`  
		Last Modified: Sat, 12 Nov 2022 04:14:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:b1f6e3101f976f2932e63ea0d8d737ee7ecc67a69cf1319a7fb56e35eac109f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb833062aea435929d61a227ba0f00aa3547e5c4f244845ef9ecf138058710f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 12:05:52 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 12:05:52 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 12:07:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 12:07:09 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 12:07:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 12:07:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f809df4cf953b3ddcfff11ca4470460163afb510f80229572d57e83e110df368`  
		Last Modified: Sat, 12 Nov 2022 12:29:46 GMT  
		Size: 3.4 MB (3442606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f27ecd002eefc2ea626a70718011fa6375136f3b1716d138cadcb55ecd8f9b0`  
		Last Modified: Sat, 12 Nov 2022 12:29:45 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:7108d1ed25b03c9b4b041b825696362edeb93cc82b5b26675038c12a2d156e8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5375216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f0043415e52987685e2532fdd26b91f0d35080124aa27979c5328d62fbef24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 03:58:49 GMT
ENV _BASH_COMMIT=31f4d468b60eb27d768ef56d0a8b4982346465d9
# Sat, 12 Nov 2022 03:58:49 GMT
ENV _BASH_VERSION=devel-20221107
# Sat, 12 Nov 2022 03:59:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null
# Sat, 12 Nov 2022 03:59:47 GMT
COPY file:651b3bebeba8be9162c56b3eb561199905235f3e1c7811232b6c9f48ac333651 in /usr/local/bin/ 
# Sat, 12 Nov 2022 03:59:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 12 Nov 2022 03:59:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55268ef2019f3fc59db6ad752944c3dab8aed148db683424e4b6b2448e13fd98`  
		Last Modified: Sat, 12 Nov 2022 04:18:35 GMT  
		Size: 2.8 MB (2783745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f880689b993410d7969c471d89c8e2d541a3e16948a11dcd3765d28cdfee7b`  
		Last Modified: Sat, 12 Nov 2022 04:18:35 GMT  
		Size: 345.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
