## `bash:devel`

```console
$ docker pull bash@sha256:476cf4fdd65f67b9cad88b4432f1b906157dc37a6212b5b3418d5f763a558322
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
$ docker pull bash@sha256:46e5e67719fbe92738642c551dee89b2e3997201d2b4352e9b2c110b28bb0bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66db8295f8459742b15a67805f38b017eafe5ca480f6c946a32a1c0bcb56e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad0fa27bee25236bb098f34e0ad6824e88dfa9fd9dbbd080a741f632938cdcc`  
		Last Modified: Tue, 11 Jun 2024 23:54:10 GMT  
		Size: 2.9 MB (2894937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0067259647a55230b4b921a650c5987775c07cc6c41527dee5be9edf34c258ec`  
		Last Modified: Tue, 11 Jun 2024 23:54:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3ca1bd4ad7385ec6c97b5dcbdf8b7c05846a7d32d856e9330361c0217752e98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 KB (122571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6accdcfab59d594fbd5baa8c301c8a244f72e387e4aa39fc112bca83a965826`

```dockerfile
```

-	Layers:
	-	`sha256:bf2270b2868dd81327c72d02b8b0baea5caf524812321a8c7f31ad9a5b8b2b41`  
		Last Modified: Tue, 11 Jun 2024 23:54:10 GMT  
		Size: 106.5 KB (106508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18e74c899a76c98addc327ac667c160d36285d76b89c689e6f8b3e8127cf262`  
		Last Modified: Tue, 11 Jun 2024 23:54:10 GMT  
		Size: 16.1 KB (16063 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:1f8ff35fc597a031f969194c94382b8baa9cddbd532d55d01ba7b68c6ae34249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6209456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171aaa6a009a1e0607b243d0a98164a97d3b1678b91df5994f402f21b489eb61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f02bb1c88a8aeb3fc904bcf2a70aa76283cb2bcc8d7be72cf3a4f3ec0a9aa8e`  
		Last Modified: Wed, 12 Jun 2024 01:11:48 GMT  
		Size: 2.8 MB (2844060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f638f7757c0130d98d12fe5e6ad43874bb75a0970a23e148d57cead7a35ae2a5`  
		Last Modified: Wed, 12 Jun 2024 01:11:48 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:315a06a58f58e9cfc447d7e07bca22e541775c0aaddf2202e647a3248687e07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03720c95e49d83cb1ba5de640b8b49cd61928f01d4b6afa410a5742d818f4325`

```dockerfile
```

-	Layers:
	-	`sha256:7751c4ccbc39cad5df3ed6b77d0aa7eaa7b5bc707d06cd0d354a6f155d6bcf88`  
		Last Modified: Wed, 12 Jun 2024 01:11:48 GMT  
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
$ docker pull bash@sha256:7ca0902e3bfc6c0f197bf7148f061e07ff48a1aca3e79998223587332b7f6563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6306807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e4236b726d7d5b0e327eaee410bde04850cfa7cd9db9312e0563d920cb8a03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
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
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057ff0468bdc7b140b44c7272ef6ca0f302c9a285c2d544d68dc0b313f5ecfc`  
		Last Modified: Tue, 11 Jun 2024 23:54:16 GMT  
		Size: 2.8 MB (2839289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d8a579934fa0a02ff568c0322f2515436c462379e612cb097ae8f27b4d6a0b`  
		Last Modified: Tue, 11 Jun 2024 23:54:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:30f2aad80082c4f5999ecfa718e806dfc227f745db344b208ce34dcc17805c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 KB (122517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9e39ffc7edfa4e6f8d77ede1fdc5644d2266941e271482d855080bb4af10d1`

```dockerfile
```

-	Layers:
	-	`sha256:58bb345eb78897a46519959ce99b0aacdb0af603126f381ba230412feb244821`  
		Last Modified: Tue, 11 Jun 2024 23:54:15 GMT  
		Size: 106.5 KB (106483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f2575b46264bc52c24d7ceb47d02ced6c3d30c4384b52acde5813831dce742b`  
		Last Modified: Tue, 11 Jun 2024 23:54:15 GMT  
		Size: 16.0 KB (16034 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:a4da62a4949c5cd0b0e6f2d8f0aab3754c1d8d51f599aede8b89d861999e0c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6737488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039f4019ca20149da0e8be6ab3ead10320fd01782ba0e6581a86f4c69f1add24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b60bef974f67b846820df63d77037653449e963a3e6547c50deca086dff61c`  
		Last Modified: Tue, 11 Jun 2024 23:53:59 GMT  
		Size: 3.2 MB (3167302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f098e9d6886bfa1f8ab5b82f1e0db907cbe9f79a25c17313296fe84802fe300`  
		Last Modified: Tue, 11 Jun 2024 23:53:59 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2e5b98204217b4ce84d8fc7a604f21abea0d752f954441cd1bbda83ac7ed0531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 KB (120689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8135475b502e78d2bf3ee3c56ceb829e0c724253939088ba02e75e839ddd8a`

```dockerfile
```

-	Layers:
	-	`sha256:72c93e1a3a2350293622cb8e82d55555565cb6642b9e2d902908f65798002b2a`  
		Last Modified: Tue, 11 Jun 2024 23:53:59 GMT  
		Size: 104.6 KB (104588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d82a5d31cb6c603bd4d48fef3996a579f97b5b81f2d70efbb49cd8b60065637`  
		Last Modified: Tue, 11 Jun 2024 23:53:58 GMT  
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
