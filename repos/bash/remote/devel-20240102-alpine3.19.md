## `bash:devel-20240102-alpine3.19`

```console
$ docker pull bash@sha256:175550a1ce961b5fdf3db4c2f05cf7cf7287caf05a8ef2acb2ff4f897c9cccd8
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

### `bash:devel-20240102-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:5310afb976ed4a34152af5835d88604f893230be0e0cb493157e109bad231f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6265904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeb96671690c4eac498f5be88bed7df6aef1797adec3e5522a4a52a0e2ac85b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25cdf221545169ad993492c8f617bf2ee86805a80677f74f4e54003b9c9588`  
		Last Modified: Tue, 09 Jan 2024 23:55:11 GMT  
		Size: 2.9 MB (2857091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f29c0d32955e306cbfcc1e5aec34f5532dae5a5c5aa05b7efe6533a991006c`  
		Last Modified: Tue, 09 Jan 2024 23:55:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3ae63f70028bd76f64d5032ae26584879d3f9518f68cae90e401dcf082f2aed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (113956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcac7d247b35395e94e31cb599d1b05a4975d65b4b0e753ed27a72d66608d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:4bc7fddc3e50a308e524e8fb4bbc86e32f4f5764606cb8793ab63f5b3c1bb061`  
		Last Modified: Tue, 09 Jan 2024 23:55:11 GMT  
		Size: 97.7 KB (97732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad389499bfaaa93ced861fd93be1c7612b2b2c2dfe948f7ca5339fc17d07bd9b`  
		Last Modified: Tue, 09 Jan 2024 23:55:11 GMT  
		Size: 16.2 KB (16224 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:7b4408a8552c92aed0256c7d9816f607611972637b51b10613c35882f9bdd489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5970606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6f4b83557f5b98b985cbbcd9e575b9bef2e21fbea7bf7d37c4c6e3ee55ad99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da21b42c822c550303ff1c6b49e57c6ab9413f77d7e4d2b655e33529f937fe`  
		Last Modified: Wed, 10 Jan 2024 00:47:27 GMT  
		Size: 2.8 MB (2805125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e57a41816bcb4731afb74d0b41370db2886da41b3b21bc8a6c2b251e70f9ad4`  
		Last Modified: Wed, 10 Jan 2024 00:47:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:00d8f7e4d9ffd653962454bbc9180a34e6298b4cd9b150ef402a2dcbf0bc3791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e3a408f153318d34bbbaab000e57bb1318edb6ce4aa542be02520174ec28cd`

```dockerfile
```

-	Layers:
	-	`sha256:8c89fc21dd38fb84335b3215f2506fc661952bdcbccb2ab91fa86548acccee4b`  
		Last Modified: Wed, 10 Jan 2024 00:47:26 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:2f164023e955cc60540daa97783f00c1f83b9bb0428aab1c332660b4c07c5c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5671520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc34f9090494326e4d63c68771356a08c47687472610b877008b7126915cb22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f9456979e3824eb01c2d7e854f8fb9e70ae5678a594d59ed6a40a33b4d1ad6`  
		Last Modified: Wed, 10 Jan 2024 00:25:27 GMT  
		Size: 2.8 MB (2752481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4c2943fcd17e622eefef9b319cfa93d2b0b99ff467ee9afc4de49d463f8dd8`  
		Last Modified: Wed, 10 Jan 2024 00:25:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b066dce78edbe8ff05940368393d4a542c833bfe7039ca1d9b95483d7bdc7484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fe941ab16ad5907f05038bf3fe6fb7ef17203956807226ffc021a05df44d5c`

```dockerfile
```

-	Layers:
	-	`sha256:6547a4e434ca08068787a22ba68c1dc74000060abcbc61c4402cf48917d9df7d`  
		Last Modified: Wed, 10 Jan 2024 00:25:26 GMT  
		Size: 97.8 KB (97768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbdc0cf9ea3ecac456101be06630d6731509fb6b70670d924f9ec6f1b5f1d93`  
		Last Modified: Wed, 10 Jan 2024 00:25:26 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:ad8e261897557dd6eab435ad6a2bbd4c459304c93660384f99a423fca7934b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6307798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deccf79d4cf98051250aac7d8e796ebb1f2f70d9c984013cc9f2c833181480b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce95f702da6b411f633ebd42aa8674277b71fb05740ddb0f22318c65e0c5a6b3`  
		Last Modified: Wed, 10 Jan 2024 00:29:48 GMT  
		Size: 3.0 MB (2959669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f656cdfc8d83e7ab54fe883926b6c7c7c0b207c9c85a4be3ff6b9f03ea216b3d`  
		Last Modified: Wed, 10 Jan 2024 00:29:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:02f80853ea445c482269ca422dd423fe57ce50f55fd5632e490a0d3561485941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 KB (113811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c122fc71e8fc44a257e2b9041d063787f45c3e97d04f963e2528f46545895`

```dockerfile
```

-	Layers:
	-	`sha256:119af789f985f089c4415748ac8cb553a1dbacb9644c4c66151537e308ffb632`  
		Last Modified: Wed, 10 Jan 2024 00:29:48 GMT  
		Size: 97.7 KB (97743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d63f0681b6b3b5f309a98b3ad7a755fd4593d685910820045ff658d7f499304a`  
		Last Modified: Wed, 10 Jan 2024 00:29:48 GMT  
		Size: 16.1 KB (16068 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:8368af809fd8e67de2b9388c85239d68bf46aff0dec431f34381a4fa3028ccb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6048601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c64789c38334b82728490cc5db108a11f85dae096bea7f352bafb76527cada`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de22e0c0ebac07a5d43d2b9d4dcd66a1f1596438b4c5839ca07162191696d89d`  
		Last Modified: Tue, 09 Jan 2024 23:55:14 GMT  
		Size: 2.8 MB (2804154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf74cbeb39565a9c9d0ce90bf74e85d097e53095c0724cf34e99ad27a7fab4f`  
		Last Modified: Tue, 09 Jan 2024 23:55:14 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:9a59290a213f969ea1e11b4d8934f3d67e3dbda51e3efb4c78ed3e494cae2ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e6d713f81d8b4cfab2dbd3fb03240903f260e4bbc020a78eb44e9a0bf1c2af`

```dockerfile
```

-	Layers:
	-	`sha256:6011eee2fe91072bbccc5e329490ba795b010d8d3d8fa2aafc1b1369a34fecb7`  
		Last Modified: Tue, 09 Jan 2024 23:55:14 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384f622e6386202ec0a9b576f4e0a3fda587380da02c806779dc5f3312dfcab3`  
		Last Modified: Tue, 09 Jan 2024 23:55:14 GMT  
		Size: 16.2 KB (16194 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:34d775ab21dc98ca79935af4051a7d794ff1cb8ba6d4025e43beb7b6a1382f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6488753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc32da371742ac4155e632a034afb0e6db989f46fd885055bf0dc06bb38efe5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0dc2d07f912244a98a2399161e7e782c5f7e1cbeb1be889bdd0be84468cf2`  
		Last Modified: Wed, 10 Jan 2024 00:14:45 GMT  
		Size: 3.1 MB (3130184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bbbab22b03ec4fbabff40e6c9cb2ab8de000fcb5fbc463c3194ffd46181fed`  
		Last Modified: Wed, 10 Jan 2024 00:14:45 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:fd6c6f6beba35fde17503e61ff5d1997f1030d7e25f1ae86f6f2e1b43eb0eca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ddc9f9512321599741ce609246d4977c9b3e420860579f84d0e552e65f127e`

```dockerfile
```

-	Layers:
	-	`sha256:4f97ec30e5590d0ad7f126c05c51eb2fdd9ea6f8283d4fec85d1f2f7ddea8f70`  
		Last Modified: Wed, 10 Jan 2024 00:14:45 GMT  
		Size: 96.1 KB (96130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db881189b5364e63526449a7b4bce4a148e2eb25662226f710842358e862abd5`  
		Last Modified: Wed, 10 Jan 2024 00:14:45 GMT  
		Size: 16.1 KB (16096 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240102-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:a9ff9aac26e9b75f60777112c8da189106d894eaa9fc720a61d58b318fbd2dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6199702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bff55d1b82c5261865d85f26fa9a657e143e5bbae6b9e79bbd63099cb03d6ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_COMMIT=fa0b002927c2897f80da762dd4196d688a46a3ab
# Tue, 09 Jan 2024 05:17:58 GMT
ENV _BASH_VERSION=devel-20240102
# Tue, 09 Jan 2024 05:17:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jan 2024 05:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jan 2024 05:17:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eadbc14dcedc641331c4315593e33e41fcc46df94221dca581b99ab7b85be7f9`  
		Last Modified: Wed, 10 Jan 2024 00:07:01 GMT  
		Size: 3.0 MB (2957034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8957040037c673a66b9fcee1d3a77e11b22f5b687e9a679d7ee62ebb68a6e3d`  
		Last Modified: Wed, 10 Jan 2024 00:07:01 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240102-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:aec2d8ab4d89cfaf9212680b1e07a43d6452fb09b2bcfbf740fef0eaa38a18a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eecd12f5b2dcd65ac7f1111bcd65eab103567d4122cb03e04588e847679d74cf`

```dockerfile
```

-	Layers:
	-	`sha256:ef9e37b1ce8cb9267d860d1c0d99f37bb7d370a1f188ce8cd84b4a057aebce9a`  
		Last Modified: Wed, 10 Jan 2024 00:07:01 GMT  
		Size: 96.1 KB (96096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65af9c9896180134de62f6c5e128501465a4770616fe53208e6b1e7b8deca6dd`  
		Last Modified: Wed, 10 Jan 2024 00:07:01 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json
