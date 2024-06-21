## `bash:devel`

```console
$ docker pull bash@sha256:70009d32df2688bbbb63f3788929758dd16ba6db0bede7c33ff681b802137b9b
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
$ docker pull bash@sha256:ae6b61f9222e68e6635607ff052cd1068e912fff7286c570c50a88f556781307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5885366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f807739c353a09f24bbe5c75b8ff14e3beb2e58c54114fa25fb2400d655d97a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2381bbee14fd4b08fdde7fae5634f60e0e558544c84ec908889b2099c5c6e283`  
		Last Modified: Tue, 11 Jun 2024 23:55:46 GMT  
		Size: 2.8 MB (2790990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589f32bbfcf5ef1a78624cc24d1ae50dd53cf780eea243dcc4c9b3ccc2b5ab25`  
		Last Modified: Tue, 11 Jun 2024 23:55:45 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:48c71a11c30975c52ddf7d4f6a96004f02756a54ce31290dda6c5df32b897c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 KB (122677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df87a80136ceb4849180c82477bdb228be42fbf19f9ee30f8eb0b59f6584d3d`

```dockerfile
```

-	Layers:
	-	`sha256:599c0781bc60cb080efb7c252d1ebce68f44395fd9faa713f3f62d921d5452cf`  
		Last Modified: Tue, 11 Jun 2024 23:55:45 GMT  
		Size: 106.5 KB (106544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03763175d20bf77fa1f22537c7300c1bfb4d709ce583374734f5b1953b27b2a7`  
		Last Modified: Tue, 11 Jun 2024 23:55:45 GMT  
		Size: 16.1 KB (16133 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:da88971416ec44659ac39fdb39c53ed1903f55449904381ef7540110b7854203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7083825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf95554848e94e1c0658f3e516cee08820f3205794eba3421eb925ade1ec41d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903341b0ebec28ee6d572414e69e947055d027a84f1b47bf450c29afa768553`  
		Last Modified: Tue, 11 Jun 2024 23:53:52 GMT  
		Size: 3.0 MB (2996713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5900b53d3b053939bef2e353d25bc7ee18fa209c6072a6f059bec602a0ccad`  
		Last Modified: Tue, 11 Jun 2024 23:53:52 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c90aabd6872236eb75582ca8b6fb8ba32c31161066b9d72afd902d1f16dc6a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 KB (122926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f31f44b4a9f81535c7fa3c56d7e11403bab2d2a646acbb5e1708a28ed7c6950`

```dockerfile
```

-	Layers:
	-	`sha256:6d8c41f2cd53c2acbecb41d3fb5bc869b0142c82f24ad39b5736c877e726acd1`  
		Last Modified: Tue, 11 Jun 2024 23:53:52 GMT  
		Size: 106.6 KB (106564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933b488ee60c9f6f3e4a7c8dd2dc394a9bd8caff0d6f16f2ab90c3e796ef4885`  
		Last Modified: Tue, 11 Jun 2024 23:53:52 GMT  
		Size: 16.4 KB (16362 bytes)  
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
$ docker pull bash@sha256:4b04c7f457f561f728e91717585b6eafa2bebd2e36038053be9d9e7a5a8f10ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6215423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73da1c5c7d87b77b7cf13e059259bb6ed31cd1cd37485766330d9e940ba176ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
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
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e93484b7c4c0d83efe90b070f85fab9cbc97ecb8254dba48815a4c026c3462`  
		Last Modified: Wed, 12 Jun 2024 00:03:37 GMT  
		Size: 2.8 MB (2846520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63bcb6e33290b7a7ce9205ea498c47b5be6cf8279d7d2bd3abb0a4bb7dccdca`  
		Last Modified: Wed, 12 Jun 2024 00:03:36 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:72a7cc95182d61e582e70d47254ff492457fa97881291964b984125ca443917f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 KB (120685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60122cf47cb4b28d852eaf05459aa9e5045ddc04b9a101add7d7fc3fbc3f6605`

```dockerfile
```

-	Layers:
	-	`sha256:76462cfed1f4298e8540b6d35f2a9a4ffa72cbf9f4630bbe29124229abfe9453`  
		Last Modified: Wed, 12 Jun 2024 00:03:36 GMT  
		Size: 104.6 KB (104584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a997e5ab274ea14641a3f6b7dccdb76155d6bba07ff7de85722adf1e18bb348c`  
		Last Modified: Wed, 12 Jun 2024 00:03:36 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:fecd30755c1798f6c006eb9441e0b32d4a84e101e5ef14d45a09e6d3e8be8eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6455941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ed1d57ecc2a46e3c3d53acc579c94641f15412d621e61615eb02e6295347d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcadccc943815cb377ed9af107a1777d778b52aaaa6c00660d2b4f5a8a6bc4c`  
		Last Modified: Tue, 11 Jun 2024 23:53:51 GMT  
		Size: 3.0 MB (2995261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27076911402a5795f48e2c3f08cfe0fac3cc84d67d223d75d7935a1c882be34`  
		Last Modified: Tue, 11 Jun 2024 23:53:51 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5e766be1766f2e87cec14d00a8c3350e76f86824237a416f21f64fcbe9df66e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 KB (120616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5460d8a80fc0a06782abbab3dc9f4026b3e39c584e01b0a7e3334cd8e791a2d4`

```dockerfile
```

-	Layers:
	-	`sha256:ec82a9eb4bc3c1b12548d484d1f4e1fc90c73a2ff041792a13c2540c995a3457`  
		Last Modified: Tue, 11 Jun 2024 23:53:51 GMT  
		Size: 104.6 KB (104554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b71f6d2a78c664a8728ff54d630b95cf233ea31a1239f10f76b79156d2e276`  
		Last Modified: Tue, 11 Jun 2024 23:53:51 GMT  
		Size: 16.1 KB (16062 bytes)  
		MIME: application/vnd.in-toto+json
