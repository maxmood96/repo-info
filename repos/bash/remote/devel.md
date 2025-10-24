## `bash:devel`

```console
$ docker pull bash@sha256:7c55e21d669030266fffb1c38172cf278b45a148fe1d38af32c6f3fb3efc2819
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
$ docker pull bash@sha256:e2192c6731370a8eba03bb4de07a0322bcd2a19b560e2de31c3e0a86c1d16718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859b0fcb39cfd43c016f7dccdb12e6e318704e3f4bd040c9b83584db981b0e00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61342bc870e6804a3d347085a31ea1fe50cc07503367f8cfa798d346450827dc`  
		Last Modified: Wed, 22 Oct 2025 02:32:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3fdd51632c2069a27323545e4238ed5d4f1346a3d25127acdf3f3b30236778`  
		Last Modified: Wed, 22 Oct 2025 02:32:15 GMT  
		Size: 3.0 MB (3000206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671852e746623a0b0d7b852edea52c206fe5fd65c9752f6820f247a6fac55074`  
		Last Modified: Wed, 22 Oct 2025 02:32:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6ce1ba38994896a1f94c7abf34cbc0f7a1fd38610c1ab874bbca2335f183cb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f83d706e6954ceb61149b2bc3cfb84b5901e11f4cda1c9698d207358268d090`

```dockerfile
```

-	Layers:
	-	`sha256:a97bb714d9fbad38742b2f61fe4535148e0ee2c9e7daf77d8935cd2de095239c`  
		Last Modified: Wed, 22 Oct 2025 06:02:27 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d754aa0c1b1274c5a7db071d131d4830299fb3474657bca7088dc5b8b2bfc036`  
		Last Modified: Wed, 22 Oct 2025 06:02:27 GMT  
		Size: 18.1 KB (18123 bytes)  
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
$ docker pull bash@sha256:80e00d284afd4cbb368254d5c65ae35b48b3c1a4938580c2b3402c390a48470f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7006646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b0d305be6af42c8908a340e1546ecc20cd2be73b6c813a88bbf4fa6db7a9fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69500dfe6b7b000e2cee5c0511b44e509e2a7009d51cdae01b1f6c9420a78a0d`  
		Last Modified: Wed, 08 Oct 2025 21:12:02 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9516e4450cf2de127eaec86bd0c4859b9cc1b4f1edf115278d853cb5785fb8a1`  
		Last Modified: Wed, 22 Oct 2025 00:21:30 GMT  
		Size: 3.3 MB (3273612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec419cea422a77ebf3038c120b45bd54ae2f81a44b49a403076a855bbbde87e8`  
		Last Modified: Wed, 22 Oct 2025 00:21:30 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:06efc730806f2a039f25f4b06d0bcad3ca8c7085dc27dbf901d41447ef44a369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ab0c4ff71197731010a62f98bab3c3502e6497f529799c811a8fa7ea755fe0`

```dockerfile
```

-	Layers:
	-	`sha256:32a33566629b49705ada262bd9408c4c6fef3984b964f4d77ef2bf77627aa3b2`  
		Last Modified: Wed, 22 Oct 2025 03:02:35 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e15d48a0b8e0b604e46d47bb1f443669c5a1b60721a4d2eb6426fe21065771`  
		Last Modified: Wed, 22 Oct 2025 03:02:36 GMT  
		Size: 18.2 KB (18167 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:8fa5e628cc674d23e1a5b3d8d8dca7f27546dce2de5f50a6a9cc322530094d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b359889db9e4ea1d0900559ce7f1cf28734ae15200c4b44e8c63ebec31db25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec7f1c6fdf9dea62e944fc5313f277694d876b6c9c5b70e1f18a51eaa352576`  
		Last Modified: Fri, 24 Oct 2025 06:16:50 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b10e80168e300f9bfb2309f9cc5e7ac52ac7fcd89de6e020ff64d253203dc56`  
		Last Modified: Fri, 24 Oct 2025 06:16:51 GMT  
		Size: 2.9 MB (2946480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d41b9df39058ce14dc0daa0b3590eec1c29aa55e28d23258ac4e104af4bdb44`  
		Last Modified: Fri, 24 Oct 2025 06:16:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0f9952c99103bf09bcf10555739d8af2bc41313743806ff542739111bb7c978d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215fb4c03ccfd9d8d73b201afbd3ee77f1cc70ba43eb202ee40c338097368a5b`

```dockerfile
```

-	Layers:
	-	`sha256:807d6b9e45de052cc98628842bf8d36d86cb4d8e3278107f824c38929ffa723f`  
		Last Modified: Fri, 24 Oct 2025 09:02:41 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63674b70a7e14bec8384966cbc90ab5e759bdcc37a8a87abe7d7961ed4013a87`  
		Last Modified: Fri, 24 Oct 2025 09:02:42 GMT  
		Size: 18.2 KB (18167 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:7c00ab86a890061787c4a1c55557b0a048a229807badbb5a298ca1cf76994787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6739822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f6d4e3deb4763ef0bc90ae956979f9d1fecabdd19cd47f1d03b077c62206fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52542f80f7eac23ac5faaa8542212ddfa07dc162276b5a71a26e1ef9281af9e0`  
		Last Modified: Wed, 08 Oct 2025 21:17:33 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf28417b7f8f428b32b602921c4c505b34d1dece143d6750a61875ee10990f85`  
		Last Modified: Wed, 22 Oct 2025 05:52:16 GMT  
		Size: 3.1 MB (3089786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc95384e67e8875fcb94baa3eca4440cc023a46f6d1689f1c93c29c8ece30b86`  
		Last Modified: Wed, 22 Oct 2025 05:52:15 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:443ca8dafd6c3f29bcaf12b8db7795327793079b7edd0003f6add92efdc4cb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dbc226beef322953a6bd38d7f18e61cf7035b813156b228d9671b236d7909c`

```dockerfile
```

-	Layers:
	-	`sha256:c1c6768feff5dea4bb62c97c892f3bee013fbb0b745f1e56047bcc8fd0c2dee7`  
		Last Modified: Wed, 22 Oct 2025 09:02:38 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b876ee8f42d4d944f76187a3e5bd184cfd4d12674a54882e0c07d36da6b0dc7e`  
		Last Modified: Wed, 22 Oct 2025 09:02:39 GMT  
		Size: 18.1 KB (18123 bytes)  
		MIME: application/vnd.in-toto+json
