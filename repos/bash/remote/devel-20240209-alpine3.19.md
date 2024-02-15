## `bash:devel-20240209-alpine3.19`

```console
$ docker pull bash@sha256:3709a67f9bb35cbc22506739aeac3b108503a0d8571ce88032df7d6235c0e9e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bash:devel-20240209-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:74036e92ce074127cad64bbde90ea3b790d807d7c6d7941fb981bbf4f1aa6b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6270647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5acc85155f2f9e0633006bd3aafa7bde5073e866bb50459f3ce4e66fb2113f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8b2f31ebb3aa0e42ead31ff8ec48944b2e2d60ff36921404ae689ce982bcd1`  
		Last Modified: Wed, 14 Feb 2024 19:54:09 GMT  
		Size: 2.9 MB (2861586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde40d0282a8e10cddc01372d599245f0b1590b8e87ea285da97c8ab50226307`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240209-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:2b351da839f3b6e025bc9851b727cd20be66de1fb2bedeee460949ebbd4b89b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21c7ecd13febed3f71066ae1741e9c5d88a17652d09ffb9ca8d7945c987c0ac`

```dockerfile
```

-	Layers:
	-	`sha256:c1869e6214a7e19f14fe4c0ceab0587f487a0585dad1dad2bc79d7e5c88c35f1`  
		Last Modified: Wed, 14 Feb 2024 19:54:09 GMT  
		Size: 97.7 KB (97738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7c740f1bafcc3b4678a16f11a7c9af1c9f2adb9c3f32302c2d38c73e001c2d8`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 16.2 KB (16168 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240209-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7ef655442b1be9bc96d18cd55ec2fce59e795c04cc6efc2d8284919596678a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6313594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051fc61fcd7be325727c40910d82c96c61051a74ceb71add9d6cecfe05476600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf089933dda9f1e084e20fab2d6cbe3c039674f3f9cedb4ede170e42a77638f`  
		Last Modified: Wed, 14 Feb 2024 20:18:11 GMT  
		Size: 3.0 MB (2965546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f972064fc51ad379a2205a8cce61fb92529ffac9809cc63938f0d8261c677c63`  
		Last Modified: Wed, 14 Feb 2024 20:18:10 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240209-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c6aa41035232014b60c4c994f0d9f5c10d6b7563a5906e4c414a277b71610b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 KB (113761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8987ca227c1e2ff043ffe2dd63d67605618146bcba0c8989ebc1c2e00177d479`

```dockerfile
```

-	Layers:
	-	`sha256:0bacbca48ac50dc1d4e9c45a7c63dc0e517c64257881e64d5c992fba6f13bbc3`  
		Last Modified: Wed, 14 Feb 2024 20:18:11 GMT  
		Size: 97.7 KB (97749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928b4a814c139cbafefc2677d333aff0dbf535d598196eb0178ffe91708c4755`  
		Last Modified: Wed, 14 Feb 2024 20:18:11 GMT  
		Size: 16.0 KB (16012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240209-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:2682dc44559c8b6caabdbc2c1e1b7a4471a2298a82f4fdd09930e9eb50184867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8a89b57a14bc81340b6652aa95f21ed49d036ec5405738f16436d791c294b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff349958c97798d90a3040c575724cddcb7ebff843e5470c8cad191ba0e3b82`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 2.8 MB (2808363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bfa5cab51f45aefd476e0e5d6378551b6fddb82263d0d5b7a273cc41e024b`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240209-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:a690ff6c521ef80d47faa731dc1dbfa84815a3f6403bbe9a9094d5404a4bc02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fe2573fab3179eb27181449339a173ab604ef0ed435017c36da93bde393962`

```dockerfile
```

-	Layers:
	-	`sha256:2c306496299bb7d14b26fee1d15bc4b8849c38d1a275469adcef5511d00e228f`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 97.7 KB (97713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f418bc7197c235d7b6752234db65a2b33fa3788e9e370b0fdf30b8ea1e4b25`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 16.1 KB (16139 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240209-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:97ef276154ba6b4e8c6988d54af3dd5d20bc9b2488e62054107e58ec77a666d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6494988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430d9061b3579e029d8e84485788b837696998e10be00d9fbfc7a0f8f6be77bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d731da25fb7ca727ab6572cba30776ce5cf23acaa587018b2696635a2a197944`  
		Last Modified: Wed, 14 Feb 2024 20:11:06 GMT  
		Size: 3.1 MB (3136298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e55d802d60c7cb05537ffc0aafde8267c55f3691f1420c1aa68f8601be74dac`  
		Last Modified: Wed, 14 Feb 2024 20:11:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240209-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0adafde3b4dabf5595535754784559a592d4dc50fbf3011d79ac4eced14073bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 KB (112176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b12a778c8a2f88ab2c53e22c65b535b70a151efbd012e2dc6783a8a6120e78c`

```dockerfile
```

-	Layers:
	-	`sha256:c1b699647f7e00f40e7303331aaa7b481273069bbc04c4791f8fdbca27737d9a`  
		Last Modified: Wed, 14 Feb 2024 20:11:05 GMT  
		Size: 96.1 KB (96136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79e6eba8bec7aab552420fd0179709bb2a9330417d631f63bb22d6804d52cd2`  
		Last Modified: Wed, 14 Feb 2024 20:11:05 GMT  
		Size: 16.0 KB (16040 bytes)  
		MIME: application/vnd.in-toto+json
