## `bash:devel-20240809-alpine3.20`

```console
$ docker pull bash@sha256:31586a938cac810b54f245a43deb3ae280ebfa3878fc0294ad63fa0675074ed6
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

### `bash:devel-20240809-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:552531bf2775a1ab93b93fe02d9d2e9c205e0783bfcb76270fbc97e07c570314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6525850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04408c034d824b54c0c974b2015f80113e82b731c1547737fc9f961f0d58ff52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e22b6d81ea43d5ac07da5411342a47d52b61688b3d623922d34cc87fb43715a`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 2.9 MB (2902626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eae15321bbf425a0e365d6cb3a2938d647f38cee38298d760cd6c95d9c7e7f`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:0669d8971120f82f65445d4b3876985eb06c58d374c318973f891f3686dd1f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced39ad6a0a498f5492281febde10b45854d2a286435d8e70b4be4262965dbe`

```dockerfile
```

-	Layers:
	-	`sha256:e58d99fa25a5a91afca861225bfdeab9e6378df128f2ee49452d05ee7d8e24d6`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e683e5459ca6b457a0cda65c44b4ad8a46bc6f1ce51ee9bb4dff098eb33a4f0`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 16.2 KB (16179 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:7cefbeec81bb157bc41c90ccebf8e025a184d43df59560bf2d9bc699c86d77ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb163665da8d7157a3df512099187665e65cd21d7efe1425079721895a0361f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fd00ca9b9b63f8ba770d033aea26601f1b1ff6ec38fb9339416dadb102c7e4`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 2.9 MB (2853402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bbf0b669e43fdf74f2205cf6e9eddfc9099b512e1426be367560e8f47d588a`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8bb74582dbf6ebc75613348830b68b6982e89fe3f5803dcb3d4f1b4758f79842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbb2bed7fbcda45b1455feaa53e2324611dd1ae40766f47a8ddfe918cb7f9fd`

```dockerfile
```

-	Layers:
	-	`sha256:fc40fc4e2c21537f216a7baf0421ee0eacebdc2f51ba5592ac1ad3f2bc6336fb`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:8039325dd146e361ecfde8e0395ce5c1946e05ecc299dc854c005dc4d6806636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5892059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6292b18cebee5cc0f4de7506350e8c21b8daf88dbcfcb49ac33b0e389d65fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852c08f139c06efff5bc6d99d5cf6bd2d2641408ed43e3922897eeda266ba79`  
		Last Modified: Wed, 14 Aug 2024 00:33:38 GMT  
		Size: 2.8 MB (2796768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620234ded5829688e7d7eccf155a98070e9d506d164dbd1e02261685ce162294`  
		Last Modified: Wed, 14 Aug 2024 00:33:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7ccb31bf565b849eb1259281679d7fbd3dd3695dbfa6017227857f83ddab6293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2d4e67c0e7482bbe6f9deccfd64cc34e9ec2668d7d936037d362cc99704caf`

```dockerfile
```

-	Layers:
	-	`sha256:3bf5fffcef88e888827b7720c683ecf692f61b8957337759bf01b27b07b7a4c3`  
		Last Modified: Wed, 14 Aug 2024 00:33:38 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49f623d76934868924ec6441cf8a6597cfe7aa6b1ab8e941db5270ac14dd1a1`  
		Last Modified: Wed, 14 Aug 2024 00:33:37 GMT  
		Size: 16.2 KB (16248 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:6a6f296a12c8849e9670244db113c634ffa9f558e1b2fad92409596c0d627ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c980a5ebf15bba3b49e1c9705acd8991b2d046324c549f311230bf8e8f08d1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c91a7188e3812afab90fe8796dbb0d3912bdbde54c9c100cf89a4acabb11dfb`  
		Last Modified: Tue, 13 Aug 2024 20:49:16 GMT  
		Size: 3.0 MB (3003700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29676399746f7cd2941c9f36ac99a14c360b03db23878dd5dfd4c3be5879203`  
		Last Modified: Tue, 13 Aug 2024 20:49:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d667ba19288fbc0bedba38849dbc01911801cc42f12ccccab782cf290518e892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac27df563c7a9f1d629fed3d02a5762d97711bafd32928516687075a5125242`

```dockerfile
```

-	Layers:
	-	`sha256:461bc570ad5948cf13dd1acc3485a894f42fbcb4956afc005b0b8a27789c8dbc`  
		Last Modified: Tue, 13 Aug 2024 20:49:15 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11b90b5691d4e7c34b137f5ba9ca75eb6b426ac3ed77ea58ac352aec5b4f5c04`  
		Last Modified: Tue, 13 Aug 2024 20:49:15 GMT  
		Size: 16.5 KB (16479 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:6310bcfe668760fa4f721f2e3889b577fa9a9068165d20d753c754e0f5b2138d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d45188c8e972f486d2740e14f5e78aa2a92e646f414c5db0c5401f33b44d892`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c869346356eafc5441bd6ccaa9dd32f056bf4d92a557c2cf038b8bdb8b362bd7`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 2.8 MB (2845752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28b39f983581ec0adc5ab93b5447c0e90c9a4e1c6701533925c9b7879540da5`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:5ee575cd6a5df30dd190a69122a4863351fa5acb3a042f5173fd18be942e9a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e77a11fbcb825d1287ae9257e3b8e73aac8c3aeb413164e27443a11624b9e3c`

```dockerfile
```

-	Layers:
	-	`sha256:d135542e3555d38116f728e441e36b88cc32ea8eeece46d525463e078258a37a`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a4d1f11e073fefeb1eb9479659f63fc8c409cca9e8b7a9acd1873d8daf7f1c`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:1ad4714d90c65448b382ba33b63d2bb7a60fbee1eeb9365e714060d559df6dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6747492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a30b2a47745ec9c09fed8d921d8c0a34ed7e6cd0e8b0d0d6281d9f3b59f08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a29cee3543e5564b309f9d50d689503440be679f90999435416622d2260c8f`  
		Last Modified: Tue, 13 Aug 2024 23:04:32 GMT  
		Size: 3.2 MB (3175604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5547b7598a9bfcf0b9cb16aa9b99fb4572bd51c9894829cd65b86a6c68f525cf`  
		Last Modified: Tue, 13 Aug 2024 23:04:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:fd668c94df32e29d4a1d4befa7e24587b2a1414746f2b534b8ffcd5efeae8591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe14c9d3c65972b60be3868e64903d457b933e04f22f82eab049330005fc394`

```dockerfile
```

-	Layers:
	-	`sha256:298f8a75b4e6a2d783a1cef8c1c2fe95e27e33be3478d0b7e3badfa666736ea4`  
		Last Modified: Tue, 13 Aug 2024 23:04:32 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c0367a13cad9616706cac98e6ee4ca8de8f43a2d59434b66411e2e3d54d35d`  
		Last Modified: Tue, 13 Aug 2024 23:04:32 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:f299a114d05782405243afc6d1b714591c3a1aece82fb4195e0b008e5c8654ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53e1ea36efcfdff9c37bf173d9381428e6432b2fd2fd639c9c921d4ff85db80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959eb4f6429b9cdb1048e97991014f239531082186631f4859f0ae62f1583611`  
		Last Modified: Tue, 13 Aug 2024 20:10:46 GMT  
		Size: 2.9 MB (2853897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdac6e9e5f470ab398e5172a78192a8504ef7ee2c7990e822355db66a69dad7`  
		Last Modified: Tue, 13 Aug 2024 20:10:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:fa87f6db1525f20c78b6b4ecaa371d4072589038c0cb2aa1ea952a3a3873f40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e9fa79ca22698a2362eb4528c9579cc4afa27e8b93f56a3ce56458197c54cb`

```dockerfile
```

-	Layers:
	-	`sha256:4e21048637594d58d06f7feb4229bc32ca32e066c04d5dd434f36f65382d29db`  
		Last Modified: Tue, 13 Aug 2024 20:10:46 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0fc4e9139f7f2dd18b09b3f461756e9a3f5e027f897f195257cf2798eefae0`  
		Last Modified: Tue, 13 Aug 2024 20:10:46 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240809-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:dae48e41010c4df4fb467c98d19ee6aebd218485398d5c4ad678efecbf3689a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed8424c8d2efc945f59fa40f61d38a8a0ec3e82fb2cecefe5f3025180b3ca1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99136c063156a228204f07bd93c32d40f38251df89ff335d1a632be96fa05ab4`  
		Last Modified: Tue, 13 Aug 2024 22:00:56 GMT  
		Size: 3.0 MB (3004364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc5da12027afd5519f56d5d3c61cd415c2cf9235948412658e67c99fcff24ed`  
		Last Modified: Tue, 13 Aug 2024 22:00:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:7f138b57523a4f162edea7b805f7495de76d4c66c5363afadda86f5130bc850a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd917631e1aa6b0179c27cb8fb23fd4b8e064ea7f2f0b18d4adb2f9819699d2c`

```dockerfile
```

-	Layers:
	-	`sha256:5f8d09c38f271c2c1d0a2a3d871f6a53f1e4a869feaf2d2b3f0cc5bf18338ac4`  
		Last Modified: Tue, 13 Aug 2024 22:00:56 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6781c0385966dbc10f412bc5df29543221068af1b99740637c695d42b567b5a1`  
		Last Modified: Tue, 13 Aug 2024 22:00:56 GMT  
		Size: 16.2 KB (16178 bytes)  
		MIME: application/vnd.in-toto+json
