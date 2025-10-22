## `bash:devel`

```console
$ docker pull bash@sha256:02969b3bff026509c069b4d3e58012dad538339acaf28f4c80262e73c0c65280
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
$ docker pull bash@sha256:52f1bacc7971d292f948fc065e8878c8e412846cdcac186c7087e90a099b0ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d0eba8284834cac6945cea1b9addc300522f968beeef0abc2c2bb01dea54f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bedb1ceb6a954e3d76a9989190501096d77ee73e10b0804e1d019bef90867e4`  
		Last Modified: Wed, 08 Oct 2025 23:07:35 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e80ec812dcb377751d93cae5a0bc548273bdf6c3a8a4468ffd4ff1dde9ca3`  
		Last Modified: Wed, 08 Oct 2025 23:07:36 GMT  
		Size: 3.0 MB (3003426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c6fac95a8943e1bd4a2cabc68a857924665d20c2fa123a0df35314e3c49782`  
		Last Modified: Wed, 08 Oct 2025 23:07:35 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b68b208947ea99024d88572074e3f10c5182c4ec5137e547eaf7154987bc2729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6627e1aaac96e84fc6607c5517d765ce6c84ced75045e7f4e46f8a52a200c038`

```dockerfile
```

-	Layers:
	-	`sha256:56e7cfab52fedc530f69e08e383553d81dac76bb32abc8b33aba31e933282f1f`  
		Last Modified: Thu, 09 Oct 2025 00:07:44 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b4e04ffa80752d58173db0dc9049225ed9d8e74172a66aec5fbc063f73f447`  
		Last Modified: Thu, 09 Oct 2025 00:07:45 GMT  
		Size: 18.1 KB (18146 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:a45b079f00d832699791c88d20998c91009095556d0b2e5c8457ccf44cdc51c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6442717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b1fbfdca8e4e5df7df3db43879ba04dc15f392d1c665ec755a79275a55723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_COMMIT=6edfd0bf647cac5c3af3c15aabf49e27528ddf78
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_VERSION=devel-20251017
# Tue, 21 Oct 2025 04:18:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e391da0eafa7076e821db267a829de2fda5a105528f3eb759ae311c58a3f88`  
		Last Modified: Tue, 21 Oct 2025 23:26:14 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f6ced113db4b8fc6735614fb75fbd8b379fbd0fc85dcdaafdabd11371a8d8d`  
		Last Modified: Tue, 21 Oct 2025 23:26:15 GMT  
		Size: 2.9 MB (2937844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6661845714182a7306525764de4af596be7e3f7c61ae398e298d183c3e87a6e`  
		Last Modified: Tue, 21 Oct 2025 23:26:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:705c9f493f0faacd4ba9fbfb7c6dba982152247f005f9174c3dd8581f3d3fdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (17988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07fa6128f38c90f5ca4a6679fada9adabd0f4ce1322e7692f27e3ec75bbb8899`

```dockerfile
```

-	Layers:
	-	`sha256:2cb5814f20a225c13ce0ea529fb6bee2f4922ea21457a7f8c42f93f85c1b03fb`  
		Last Modified: Wed, 22 Oct 2025 00:02:41 GMT  
		Size: 18.0 KB (17988 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:3dab99a72d185be1ba012da15b3cf6c7ecca7f37efcc61f2f30f1d11fbed5a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6111797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fd183169971d1103a6e2a2efd0ea16fba950597f3d44b255ad8a57ea4cfa26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_COMMIT=6edfd0bf647cac5c3af3c15aabf49e27528ddf78
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_VERSION=devel-20251017
# Tue, 21 Oct 2025 04:18:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b780f97615ba6a42d268d9ce3a584cc4c1f45bbbc00b9b4af2da1c540f1e800f`  
		Last Modified: Tue, 21 Oct 2025 23:26:14 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0185cbaa6a0b0e7ba618d8a959c167cc85ee56509343f9dd1c584959d3c2bc`  
		Last Modified: Tue, 21 Oct 2025 23:26:14 GMT  
		Size: 2.9 MB (2889446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e81d815933cd17893793924553d098c9d48aee51c62fa98d8f582f469e14b5f`  
		Last Modified: Tue, 21 Oct 2025 23:26:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:78b95c8917661ed7f089fab8c28781ca0f221c6c9ec18a224b557c5b57c81db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fff75fb092e8b8c04eaea7ef64256732eecd8ea52bcda477743d7484d5037`

```dockerfile
```

-	Layers:
	-	`sha256:a6cea7b64e2704ce1f8bc4d17e9599f320433a068f1419dbb93a2e2965b892d7`  
		Last Modified: Wed, 22 Oct 2025 00:02:44 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6aac80ce15bc6827f02f55bff40170c95434e05e7a26964f0aafe9a340832b2`  
		Last Modified: Wed, 22 Oct 2025 00:02:45 GMT  
		Size: 18.2 KB (18203 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f09af08fe75314417ff84a3ed824778fe2065b89b219f0335afcb1d0131d145e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0f864129b261299725b481257b573e0035eda537417a03f92e85ec26d2c1b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_COMMIT=6edfd0bf647cac5c3af3c15aabf49e27528ddf78
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_VERSION=devel-20251017
# Tue, 21 Oct 2025 04:18:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c139ac6c288eb95d253bed135375ab356a8e5a0946bdfd0f09448d2b2f5f9`  
		Last Modified: Tue, 21 Oct 2025 23:36:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caf09774b05b56b82ca1feffc123bddcc681f518af3f6da4d8979aeedffa271`  
		Last Modified: Tue, 21 Oct 2025 23:45:15 GMT  
		Size: 3.1 MB (3089283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cb85160b7acb618ab89c60b335765be016efe487468fbcbf748f8e72b77967`  
		Last Modified: Tue, 21 Oct 2025 23:37:02 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cf2b19c234a1645a0c070717c24e24ecc6a5974961f3415eb0ef27fe843a6e8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c94682c73a7753b1035d363ea6c2903c767fe0cad54f02c2f7865ebb35652f9`

```dockerfile
```

-	Layers:
	-	`sha256:f40ee81ea37b73868f9b99a06e9b5d7f93570d5dcc1ee9d724157957429f1f1d`  
		Last Modified: Wed, 22 Oct 2025 00:02:48 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d11fc47afbb34e764082e1c5d9bdcedb8e1e5b92115decd839fe8612f5edf0`  
		Last Modified: Wed, 22 Oct 2025 00:02:49 GMT  
		Size: 18.2 KB (18227 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:dfc397a617974fce10e63e8aa5e5cf332650eb44923654efaea410a7de21b793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6545492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8a55eadb542dec4363b6ce2a7742e9d614da8cd84854b10dccad6fdbbf4106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_COMMIT=6edfd0bf647cac5c3af3c15aabf49e27528ddf78
# Tue, 21 Oct 2025 04:18:23 GMT
ENV _BASH_VERSION=devel-20251017
# Tue, 21 Oct 2025 04:18:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 04:18:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60b87be6930294993877b27e20a8de1530e36a43eb53000c9afd4cb86cb64b8`  
		Last Modified: Tue, 21 Oct 2025 23:26:50 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945982f7a32428b4fd7dd3aa6888b75aff8dbfce18783f722f50a334f340e0c`  
		Last Modified: Tue, 21 Oct 2025 23:26:50 GMT  
		Size: 2.9 MB (2925768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4952d59fcb593c1b3ebf24fe877a14712bb8eb7c9bff56dffff5f71ca5618b42`  
		Last Modified: Tue, 21 Oct 2025 23:26:50 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:75bf915901e75446a2f75c49ae1c63279a236762ad47b15e726d0e42232a1467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e128785b98db4832539b90d4abdb5fd538f4f7fb76ab79f14e3148c1c7e7c27`

```dockerfile
```

-	Layers:
	-	`sha256:7ede008ccf0839efaf82cbb8ad61ece7502d57f6c92a7edae749bc59e58940ee`  
		Last Modified: Wed, 22 Oct 2025 00:02:52 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98fb1bb99758770d543433e17463640f5751fee453415edddc78ee30a8deb181`  
		Last Modified: Wed, 22 Oct 2025 00:02:53 GMT  
		Size: 18.1 KB (18089 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:7b23690250822659955dad9fe3f0891990e8e41af78727dd81008e19b47e4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7009716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96f734659f8d652984326edac1815247516531d5664992901e3606c64229ac8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69500dfe6b7b000e2cee5c0511b44e509e2a7009d51cdae01b1f6c9420a78a0d`  
		Last Modified: Wed, 08 Oct 2025 21:12:02 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59480d86251ef4f957431f84c6bf7757bf913629e79e2baeb6b1151cae86f396`  
		Last Modified: Wed, 08 Oct 2025 21:12:03 GMT  
		Size: 3.3 MB (3276684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330d595490a4d04b99ff22e57dd8882f9ef3122081ed05ceacda05279f479a5b`  
		Last Modified: Wed, 08 Oct 2025 21:12:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a8eafa98511d9fccab1f9bb91f4b7d8f6384df642bc9af47f91f6c9d0a080d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd742d2e0bc83c16c15ea1ecdc7550504f81b0b250638b8de7b205b7e1ec37af`

```dockerfile
```

-	Layers:
	-	`sha256:ddcfc010cae89a32abea38a70ba54ccdda3edafdff8c997e916f5c1cafc7b2df`  
		Last Modified: Thu, 09 Oct 2025 00:08:05 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a782bc34c187ff0072c12b244b2faca13b1fca1d5290a19ba44983b58857845`  
		Last Modified: Thu, 09 Oct 2025 00:08:05 GMT  
		Size: 18.2 KB (18190 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:02e06154f624910ace857de964521e92360f97a188c2f7b763c24b9a159b7151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df1c3d3da81728e6045e0aff938e48e764baba35127af575eae8789fd2b4436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125a0571d69acffa5c2fc31545cc552342d248d34cc6a400b72035cc99d44e8`  
		Last Modified: Thu, 09 Oct 2025 00:51:35 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe7829fe4d446ba75ec610d1ad39956c2945c121bf707f6ee6f66afb2f9530`  
		Last Modified: Thu, 09 Oct 2025 00:51:36 GMT  
		Size: 2.9 MB (2949107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ec2b6d16eeb8e3874ee4d6b0e6c0dfc9a1a89f548e0797c1ebc054cdc82a6`  
		Last Modified: Thu, 09 Oct 2025 00:51:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7901d8c5cf4dc4fb0975504f9d6dcb84f6f8242872bd9950f8140525edf82ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ab9ea046cf5b79d793c2bfe3c3cf88edb08b5bc351fbc3fc7a6a50c4562669`

```dockerfile
```

-	Layers:
	-	`sha256:cb3b0d70f1e39acf59ca4dda02700e0dd62cac5eb7dc2649bad2884602f3f689`  
		Last Modified: Thu, 09 Oct 2025 03:04:53 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b2e9e5d3ddce50ead1b365d8347d3a3fe18bf14643fe70168f696315ea2e93`  
		Last Modified: Thu, 09 Oct 2025 03:04:54 GMT  
		Size: 18.2 KB (18191 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:19d46c5d66f5dd4815bef96fe1ad40a4389c4ddb14ad498955ddd4143681449d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6743810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e854d097dbc30aaf77746ccc37da956463cbab287598450a4a2f2232946369ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 07 Oct 2025 04:18:10 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["/bin/sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_COMMIT=25c6aa5b230167c6471898539c46dd2891d891a5
# Tue, 07 Oct 2025 04:18:10 GMT
ENV _BASH_VERSION=devel-20251006
# Tue, 07 Oct 2025 04:18:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Oct 2025 04:18:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Oct 2025 04:18:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52542f80f7eac23ac5faaa8542212ddfa07dc162276b5a71a26e1ef9281af9e0`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bed56522b0b65afd1bfe1a1bc721739027b0efa143f22e7babc14b7bab8d989`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 3.1 MB (3093767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d683f76cbb555179c10455b1165e32708d8e46ec3dc52c0e6b088e828c243fd0`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:24258d9427a7ee969766600d371d3aea66e06cd2b1f9c92bfa8303d6d483f51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630e044f9a5ff805e9a8b459ffbf71253d3827baddc8c910516b46324af1d0c3`

```dockerfile
```

-	Layers:
	-	`sha256:00a7ce71c0ab83824b82519b1a72708e83d77f6853ee2ee2a94a6146106e393b`  
		Last Modified: Thu, 09 Oct 2025 00:08:11 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c63f98defecc620b999abbf03b8a0f3262e9cf80dbed3171b5e15a3b0053b6`  
		Last Modified: Thu, 09 Oct 2025 00:08:12 GMT  
		Size: 18.1 KB (18147 bytes)  
		MIME: application/vnd.in-toto+json
