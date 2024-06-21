## `bash:devel`

```console
$ docker pull bash@sha256:40dea40dbe6dc17ea6d8e7f865362130df3d1d2aa17643a0c8c4e97ab8f033c0
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
$ docker pull bash@sha256:d5724f3fe56eea89080fbf5d8af8a631162911953872ba1b341e5e6a4d00ab95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6519133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c1c87c9d03d8f7e1d931b244c6613106e74698c55390477b817a2807db72a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f942e768bc2a1e24ac0d29429762e1a4faefb3c5e2c54d4c729b0bb5a067ab94`  
		Last Modified: Thu, 20 Jun 2024 20:55:24 GMT  
		Size: 2.9 MB (2894953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6411410f3bbe9b6b296faa963f7a0c72b52a3874d38b07c60bb1fb532e0bddf9`  
		Last Modified: Thu, 20 Jun 2024 20:55:23 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8446793781770b3c2758ef26029179232112fc7bc1c3656928648051b6d15647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 KB (122572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16bb370564fe09e0789aa67055cf21e6cd3fdd986a604683e68560155dc880d`

```dockerfile
```

-	Layers:
	-	`sha256:8d6b11a03557a612d82fcfb900e52a8b70889d5a6c4745f9d1ef5301bc99e91d`  
		Last Modified: Thu, 20 Jun 2024 20:55:24 GMT  
		Size: 106.5 KB (106509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f4494ed4cbdeafac7912aff91b59b80c0ca2583f3ccf397e1b37d45ac980c5`  
		Last Modified: Thu, 20 Jun 2024 20:55:23 GMT  
		Size: 16.1 KB (16063 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:73b1f6f6e63987366776080e1afa9b2789305c3745894650af1ec307c297c3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6211533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa346440ed733cd46a8a859c44f2a70dfca4b789e21bf5d83f3af84ec498998`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3fa968090fefdd4ae07d19e581973b1687c8c7978d24396e54ebe5eea0ca83`  
		Last Modified: Thu, 20 Jun 2024 21:58:52 GMT  
		Size: 2.8 MB (2844041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6110e1c9c962a3d40a5439ade652072b9bdaf1721be5668f8d73fd5f0b3cbf6`  
		Last Modified: Thu, 20 Jun 2024 21:58:52 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6ae12532b1177ac897b24b3c2c6ba431a97a38253aa38edb4cab6bda3df053c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e163e41a7c0369d172a9169191e46197815f318f9478edebd4c0729478e4b4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ea3f846f5a28dfbbcd9ff75ef4efa4733865f90de324a717558268910f98dc0c`  
		Last Modified: Thu, 20 Jun 2024 21:58:52 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:375f46674da78bc5579abc1446636de0bb44b91fa65a44541a3277d08035fca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5886198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b044ac3d4f11380df3445547f959b7dc545945dcbca3baf580e8eff576c87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2c69dcd4bc39f316d1ab40c61529127ef2e6c8360a47ce601dc78225b46ab3`  
		Last Modified: Thu, 20 Jun 2024 22:58:21 GMT  
		Size: 2.8 MB (2791005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb9e4cb4c4dfd5d3592705bb2f731fcaa8d646fd5baffefa088e93c09798473`  
		Last Modified: Thu, 20 Jun 2024 22:58:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8df10bbd644fe41ab8a5a861e5a5f0e44152e3715c984a6aba488efe048f755d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 KB (122677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d0391b882f8b94390c045c9705102678c0bb7daddb9c2cf26bcc0c04fbe8f5`

```dockerfile
```

-	Layers:
	-	`sha256:4d6c47de3aa443ec1ee33ce65db82b65b91906c15d15a50d57e30482656b9fc1`  
		Last Modified: Thu, 20 Jun 2024 22:58:21 GMT  
		Size: 106.5 KB (106545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:648364e5cae59b37f94788dcac55bb286844c096de6a466d090e61652cc3c30a`  
		Last Modified: Thu, 20 Jun 2024 22:58:21 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:e25c0aa19dc91171e93f2da1345d11e57e4494dca6fce824927e1463c388bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703befe3fad85c13a3351d5c90e61cf22cbb857f363899d90a5cb55fcd9f1108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2a95544744ffa34b37450546264565ea0e63b4556db7774944c8af26313374`  
		Last Modified: Fri, 21 Jun 2024 03:39:34 GMT  
		Size: 3.0 MB (2996713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3473b174f1a04bff5a105f2f5f4a2f5b0a93109b8ddc1d594f6e7f1e3a0051`  
		Last Modified: Fri, 21 Jun 2024 03:39:34 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:922f692a68913baaacbc27c4ef6eb0063e5f2baf8780c008dc34c779b1b88fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 KB (122928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c66f98557443eacf58bd5891ab7b3f13e5ef715e9e18518ec84eee00885aac2`

```dockerfile
```

-	Layers:
	-	`sha256:1d974d45013a57ef2bc1581303420c91cd1d7bfddef232aa9f3bc1a7be19d0af`  
		Last Modified: Fri, 21 Jun 2024 03:39:34 GMT  
		Size: 106.6 KB (106565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d394f460e37fcf4d37ac16f3c125a4c3a5a41675aa4f4e28aecbb1beb078633`  
		Last Modified: Fri, 21 Jun 2024 03:39:34 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:18aa14427158bdeacc8961c8007d23a47fa952c023d699251da35d65924be1d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6309096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37dc3df1539c100a61e482835daf4347a3a4b0f269eb9fe7e35fc1a1a5bd0ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0289d12b19d6f07f118c1a8203bf4886709eb5e2c6c8a7648ad4a7c6037af11c`  
		Last Modified: Thu, 20 Jun 2024 18:53:55 GMT  
		Size: 2.8 MB (2839290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376865bb4bc58fe12d1bedcd01f96f373148190739bc977ecbe0bd358e35ca7e`  
		Last Modified: Thu, 20 Jun 2024 18:53:55 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:38cfc91d8c234c0b4c5f3701668278e7975f4b7984f23ee50dc7bde601d1fadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 KB (122518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a18d3b6399a03d85d1b34fbda0203894e8dd41122714e094663f0524362262`

```dockerfile
```

-	Layers:
	-	`sha256:2bb9737faa03655e40110e846b73d0cfcbbde9543417e2743651aafbcc6bdee3`  
		Last Modified: Thu, 20 Jun 2024 18:53:55 GMT  
		Size: 106.5 KB (106484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f55f4947ffff7015ff41afe75420fffbaf8d9932f5fe681a6392e8c9521c126`  
		Last Modified: Thu, 20 Jun 2024 18:53:55 GMT  
		Size: 16.0 KB (16034 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:16da3efc1b1ac1a1f303656d194b6ef7b0819d1964b08ac0e0c319b9d0b62750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6739317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aced431eeff63ee94e06691cbe1b8f81040f843f4b7e8fddeb48327e6a59441`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb9a87e1f22a4b159657fb3824ac285ec710a86a9d5aec61f48dafb0c2cd6ac`  
		Last Modified: Thu, 20 Jun 2024 21:00:47 GMT  
		Size: 3.2 MB (3167279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c72412082c68465df016329d705b287c732bf3dd0157120c9787c7341b5027`  
		Last Modified: Thu, 20 Jun 2024 21:00:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1260316da3ef3743f8766cc3dfe40a67dc4bf1edeadca7017ee529f115e56cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 KB (120690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27ef63871fb42c409767adff7ba5c7c2c0ac7d3cf39cac523f357e7bafaeb94`

```dockerfile
```

-	Layers:
	-	`sha256:25b8ea297f262bd42b677a6fbef025ac378a2053b0d0e7fa831de117cac197b5`  
		Last Modified: Thu, 20 Jun 2024 21:00:47 GMT  
		Size: 104.6 KB (104589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef76fe4ab6b58a240d343070d0bda437c3fdc72df54c02865f262a9e94c0fd8`  
		Last Modified: Thu, 20 Jun 2024 21:00:47 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:c4f803ed14b05e0b9459f38a1d3ce50f7c5a4cf37cf53097c2e2c614236a7050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6217950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5eefc966540df607cf0ca960ba6746748128e3d71703287235850a6f61f6b35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ac2ec989637a3a07615904a83d7374f1f689f30f6dbfe7e7aaf4a21e623e58`  
		Last Modified: Fri, 21 Jun 2024 03:42:51 GMT  
		Size: 2.8 MB (2846572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37448e62b875a008dbf4552a3fe4f46093057664ea5fe939b5c36d93c68d086f`  
		Last Modified: Fri, 21 Jun 2024 03:42:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0564ed59472e79d993618ee8ffe1241b965de97f2310549ce2077872052d6af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 KB (120686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457fedbbe237fc1e0384b0af6c73f8200f3e354610750875879cf4618149e5f3`

```dockerfile
```

-	Layers:
	-	`sha256:c5616df95cb16de1f093788cf8a68e3738dca7c9165e13a4354260a522676d82`  
		Last Modified: Fri, 21 Jun 2024 03:42:50 GMT  
		Size: 104.6 KB (104585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea54e58598e6331b73841e4eabb548f11fbc79c0d88c368d881e6e0a2433fa4`  
		Last Modified: Fri, 21 Jun 2024 03:42:50 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:d5b7e94b09e602dfb466e84bfa3cd3b4f196038e00d5bba8a850e8357b1b98d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6457457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f2b47349d9f175a78da4e6075246373c3bcdadd845eca5696b0795bfa53c79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Jun 2024 04:34:48 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["/bin/sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_COMMIT=dbb48b978671394bcb33c9f34656a9aadf40a318
# Tue, 11 Jun 2024 04:34:48 GMT
ENV _BASH_VERSION=devel-20240604
# Tue, 11 Jun 2024 04:34:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 04:34:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 04:34:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3d263f82648f38340576847274e4139f80d6c5a2a8e12979f43fd7c24f7ec`  
		Last Modified: Fri, 21 Jun 2024 14:08:36 GMT  
		Size: 3.0 MB (2995264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98402c978b2baa9d761b49d740b623ebda3d73efe6c1641d792b271ff05930c`  
		Last Modified: Fri, 21 Jun 2024 14:08:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:592e181bde503ad93733cc6af2145cf1f1e7649ad3171d9236fbfa2bb99ce371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 KB (120618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb330dc64641ca5ba7028e6297e319e1493faf98ab4d36b8f43c9423f69cb6d`

```dockerfile
```

-	Layers:
	-	`sha256:89fb95fdf9fdce17fefcbb9a48e04c83801ae8330a6e90bfae1c42efcadd71af`  
		Last Modified: Fri, 21 Jun 2024 14:08:36 GMT  
		Size: 104.6 KB (104555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea5364bded066e5afd9ce60dc236e3044a94711efe1e462eedfe2a0c83f793a`  
		Last Modified: Fri, 21 Jun 2024 14:08:36 GMT  
		Size: 16.1 KB (16063 bytes)  
		MIME: application/vnd.in-toto+json
