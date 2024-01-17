## `bash:devel-20240114-alpine3.19`

```console
$ docker pull bash@sha256:8671026889c1b6c99ea6ffc7ab6e91a84d28d91cd05a28e53f087ebaa3613f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240114-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:938f2fd99c425ec6be26e11608fc7988bb1097e49f81fe52c8c5d7bbdd2982ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6266158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60dd837eb69428140889482cfd6bcb513821cd023a90d055ce97b349102bd653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43ad87fde2bcc60ea847a83dd722327ffaee41029a18c1e34a16e7b7544c5e`  
		Last Modified: Tue, 16 Jan 2024 23:55:52 GMT  
		Size: 2.9 MB (2857344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc513a07c3387b196ca065b4ebdcb146ea27823c5bbc69f28374558bb03038d`  
		Last Modified: Tue, 16 Jan 2024 23:55:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240114-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c8556050a22eacb99fb57aef13d5cf8b26448c304cd61b536c0ca0d4371beb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab1d9834de64c2958b73fb098e364553ae945b8cc9699687baa97ffbe0f3b36`

```dockerfile
```

-	Layers:
	-	`sha256:f9fe3171e85b854c94df239c2d487c9417bbe8b798f9d99020a37759646db2ea`  
		Last Modified: Tue, 16 Jan 2024 23:55:51 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea51efbdd84657294fe0c01d8d8d61e32bb6f83bc1b77181db62a2fd31e62d75`  
		Last Modified: Tue, 16 Jan 2024 23:55:51 GMT  
		Size: 16.3 KB (16264 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240114-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:6521079f0304798902536dabf2ca9d462fca3e5ba9ab1fbc85a76d678faa054b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6308640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52769efaf146f2102d014a6d69f8c1f2c341174497da3b1163df0b7479d277bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eafa7e16f5ce37082f5f95f06fff15fc2f380bc19725a1572ebb9e431878cc`  
		Last Modified: Wed, 17 Jan 2024 00:56:25 GMT  
		Size: 3.0 MB (2960513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202ae6a865705161bae46773f8732bd35557eed89c5a191d26c4842ddb3eeda2`  
		Last Modified: Wed, 17 Jan 2024 00:56:24 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240114-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:33583587d5864af17b053e49bb1d3f416e6ae6caa21b31ed51037c8fa35dd0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a601422eee654d19c861d6ae31485609043536c725849c7ef1d5d31d39c7ed`

```dockerfile
```

-	Layers:
	-	`sha256:6891670ed6c048cc585f6232e474944a78ca5df6caf9a7a5377a9a829f19f610`  
		Last Modified: Wed, 17 Jan 2024 00:56:24 GMT  
		Size: 97.7 KB (97743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae50ba985146b37caa009ee1f57e6d2766cb1961113dfdaf51996e760d417ac`  
		Last Modified: Wed, 17 Jan 2024 00:56:24 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240114-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:b8ac72f17595857d7c1f9400bc38a3f8af40c2af5c03c000e800cfcf3f20d24b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c734c677d6f003b26a7f932ead9ca1819825ab235c210f3de43f16124302eec1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab90ec8b876f8a2ced4ce142b4bcd18e7f63cec13fe0fe84ca5fdf3ea271c02`  
		Last Modified: Tue, 16 Jan 2024 23:55:52 GMT  
		Size: 2.8 MB (2804434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc513a07c3387b196ca065b4ebdcb146ea27823c5bbc69f28374558bb03038d`  
		Last Modified: Tue, 16 Jan 2024 23:55:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240114-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c0f9366d776805f5db81295712c6e4a2e969becd2a9785198c3bdcd99d3910d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4960af45b6d8b5ab27288994ddad94db7352e9dbccfcab663c3018461ed2b32`

```dockerfile
```

-	Layers:
	-	`sha256:cc067b6eaa29c67204bb2af0d300fdeab186ae0f55499d990f155c75b182bf7c`  
		Last Modified: Tue, 16 Jan 2024 23:55:52 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73f3f4307e1aee66542065d4531818f73e419569042ebe95b424aec6f91ac0d`  
		Last Modified: Tue, 16 Jan 2024 23:55:52 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240114-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:80bc6440e7a288b5bb95ab0ce93ccca03bf34d21055880a1f6df68088d394dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6489025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cfa716ece290df1d34a56df827091ffc8b2fc1162070a81c540ce0f0d86d027`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1d8ffa1a2ae0898c8f4ad65f442c6ac81fd19e713fba6e28b6634486d1b025`  
		Last Modified: Wed, 17 Jan 2024 00:16:04 GMT  
		Size: 3.1 MB (3130456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2982986b8ac4e50f1b9e434990d01482bfd62e40fad989db88613c2a96f3224`  
		Last Modified: Wed, 17 Jan 2024 00:16:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240114-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0f8803f57d32486e3129ff35b229e0b67645e8b26c38a9001d205dd87d085e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc8a5580070ad8e5bf6b376bd172318522afdf15a67342f0a5ac901537b8aeb`

```dockerfile
```

-	Layers:
	-	`sha256:acd31673ecc34e66b8babdc82b2a343577701c455837c6fc77809c81059a0900`  
		Last Modified: Wed, 17 Jan 2024 00:16:04 GMT  
		Size: 96.1 KB (96130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5354bca050f3ad3258f513a6df867a37621eeecddfe4ea1b817e77fe2dc295`  
		Last Modified: Wed, 17 Jan 2024 00:16:04 GMT  
		Size: 16.1 KB (16135 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240114-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:61f88e30ae1bee2572bb3c89b3882b06615cd70ad44e4f77551ae10c28f0f37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6200145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9806744f06b474bebe8cf50d493531ff760d3b1637898a9900bdbd7cff5f954c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_COMMIT=f2fdb5e31317bf5199814ae9866debe1c20cd3a4
# Tue, 16 Jan 2024 05:18:09 GMT
ENV _BASH_VERSION=devel-20240114
# Tue, 16 Jan 2024 05:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jan 2024 05:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jan 2024 05:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e364b15b899ebccd5a4e4c6588cea851d532fc3a9106fae7fa94281397f97cd`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 3.0 MB (2957477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813e881bcdde0699bf5c0205fc3afe69b3d73de3e558d02c8160a6633cd2a369`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240114-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b527ed7c8a5fe3745a232367d6d18e8f86fa3b357f66b9f90b8ada24e5b8b724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8cef751df290f1379f312d095dca9683a5d5b8bfe22d051b19e915c4226ad7`

```dockerfile
```

-	Layers:
	-	`sha256:792c5922f7c945fa8395f9b25d0f4e76d25420cc53462503e673a137c92880ca`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 96.1 KB (96096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f4242fe4db6ac8bdef44ce1d1104af265453e0e1e02387d9ac965333e6153b2`  
		Last Modified: Wed, 17 Jan 2024 03:06:29 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json
