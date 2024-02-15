## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:ddf7557c8ba27c2bdc023945261fd218c178b990727c48f74643f74894ca7eec
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

### `bash:devel-alpine3.19` - linux; amd64

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

### `bash:devel-alpine3.19` - unknown; unknown

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

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:b4b37e93f3b035c485c8557ef340b491aa710314da1a1c0f6ea2214d03ed2c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3104f9607a40400f700e292753df73e624963aca93cd6e8a9ae83c73dd5b2e45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64483d37ffb20be6571922ac89697486e8f0592f6bb33c46c91d76bcc80aadf9`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 2.8 MB (2815371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9b17ffca7a5aedcb97c0f7b4bc6feca6ce21063d7f1ab7d5f6b386f198205a`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:536e14a037cc34616c32d51875a23e723bd7387b2adff543124a1e1ca55c37c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185b905c7d8b66bf56fccf67aa8b275cccaf30c5cb10da1d69a20faa527c3817`

```dockerfile
```

-	Layers:
	-	`sha256:b87b907624920d4ad247a5c56b69b40095048137bd62b5318f9291c0dc604622`  
		Last Modified: Thu, 15 Feb 2024 00:54:17 GMT  
		Size: 15.9 KB (15856 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:1662c5a52a4b6a409e1056fdafee924e56505f02deec6115e25dc6bc78c40ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5681997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5071499aff3b8db2fadfa4448879477dbb918e8edae2b125dc2db9e0e094bbd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39332213a9c9ff5e55f3b1dd79e467b712301f8aad7b6a5381ff3bd18958f0`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 2.8 MB (2762761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958384b65facfc72616cfd2de95db2b8f39f479a72cc6e30e92f3f963cd05a02`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0d8eb4faacf8c4cbac9ec506d9f37249d68508376e5a961c8ca29b8b87554dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7323eee9659c83f03fa786e31a25b1b81b518a9d760b243e880b99689a72af3`

```dockerfile
```

-	Layers:
	-	`sha256:0528a1914ce2c7c06ae34b3da240edb72b889cd04c331d27e3796f855d71cd63`  
		Last Modified: Tue, 06 Feb 2024 21:15:43 GMT  
		Size: 97.8 KB (97774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901aa743294bd7e455314a2a4bc43416a2c74193e91b09c4697547db27e4a1a8`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 16.2 KB (16240 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

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

### `bash:devel-alpine3.19` - unknown; unknown

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

### `bash:devel-alpine3.19` - linux; 386

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

### `bash:devel-alpine3.19` - unknown; unknown

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

### `bash:devel-alpine3.19` - linux; ppc64le

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

### `bash:devel-alpine3.19` - unknown; unknown

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

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:187f2a7cbdb3c4854beb5ac917d8c11eb6857d8071a3b80d66c5649421676b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370e33b802232f971179c679457feed58a3d263ad3e47c0ff9397f1ea5a248ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08645f5ad5e1a8b3e99c138f2e849d2009892158f5a30980ccac253c4866727f`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 3.0 MB (2961454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b82ff5658f91ac798685312b3a5282702af2366675b25f0f245b2a14abc8d`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:64dbaa95de77160f3590ab8aff4f61416aa89c5dfcaf820e22ec411719689c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0940a9f384d7eb33ea77146ee5a6f2b7201886d23d0c12514dadfe952d4dfb`

```dockerfile
```

-	Layers:
	-	`sha256:4425672f0629b9c5d4dfa0e1980c25aba71059f008747c8af9a963adc6a9ad46`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 96.1 KB (96102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438c766799eeea5d764dbb5057b2d75cf12633b4c44c574924796286df68362f`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json
