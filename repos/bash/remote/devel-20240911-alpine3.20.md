## `bash:devel-20240911-alpine3.20`

```console
$ docker pull bash@sha256:d2b8f9587b815dcebd9470535748797f922a1c829eefb4c2c614e97978468189
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240911-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:c1a2ac3b88153d03ec06c0a6369efd624cb2c84811dcecd864accd6fd8d6a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67938842f6eb21126b6f505094338c39204942a88a3546f44f0b9ba935cade7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_COMMIT=bc5ddc8698d56df588fd99864a650b834426ccf7
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240911
# Tue, 17 Sep 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d1a04ed889743d5154cd1f587219f95a9223ff0e58228e7d92f15cb3122090`  
		Last Modified: Tue, 17 Sep 2024 22:58:45 GMT  
		Size: 2.8 MB (2798731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08f5e972200e7e067cae07e7be188bf10e21d990f209cd8bdcd2e7dee5f89d3`  
		Last Modified: Tue, 17 Sep 2024 22:58:44 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240911-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:46a42566563d6cbefe7466dcb145fb91f719f996d8795b2fdbd48276ee8c0592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2018e7eed9ca5dceedabb9963af5795c616f79f17ef282393a6520739fd2d16d`

```dockerfile
```

-	Layers:
	-	`sha256:146b0e45ceb1f623fb4b03794601521cf077b8206ab15a4db54f9de6497c5903`  
		Last Modified: Tue, 17 Sep 2024 22:58:45 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f8c1527792bfa4ca61aef34bfdabee1e8ed112d65d1af067d75245cc5d832e`  
		Last Modified: Tue, 17 Sep 2024 22:58:44 GMT  
		Size: 16.2 KB (16241 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240911-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:c8022b5cf8b6609e201e92eb664a4847fb829c9348a392db7fde7504da7dc6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9af37eec9d4cd634d15bb952e7d110e35eda00fcdca4d9e476e48bef069ffd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_COMMIT=bc5ddc8698d56df588fd99864a650b834426ccf7
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240911
# Tue, 17 Sep 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae60d23bff0c4149c97c063a353a7b9cc626b80fee328956dc76972f6b29a9b`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 2.8 MB (2848530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c444e118e3a9f5163e471442eb98955e75ad1428d01a4c337081ef53fd8cce3`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240911-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:462e38705c6939b0d9bf9a62056b5717d07f6351def439aef863f308b77602ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (125999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7623db49e2e8bc77116525c6c6412d57ee3b12976573e273b786fa8bc064d65`

```dockerfile
```

-	Layers:
	-	`sha256:7149b1778c45e1daa94219f4511f461eb0aa2ffc60ea4adaf4cbcad6ae49cbde`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792405616669dde0c8084d642c2b6f398ab42d4a6e477ee15ddd4d634b6dafb8`  
		Last Modified: Tue, 17 Sep 2024 22:59:04 GMT  
		Size: 16.1 KB (16141 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240911-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:db55b04c5a0d25e9ca7ffdd88d5022f1a72b48b9a4fc0ed7458e22a368c7ee99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ff28c69395acd16bf3dfc35994f8a4317eaa1b7dc7a4c8bc9d240c1e0d897f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_COMMIT=bc5ddc8698d56df588fd99864a650b834426ccf7
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240911
# Tue, 17 Sep 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca372b630d44321252cfe1ef0a8bcc38e828e96e6b19f0fa2821e92477747c63`  
		Last Modified: Tue, 17 Sep 2024 23:05:29 GMT  
		Size: 2.9 MB (2856481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdea57e7cde4be8692ffd8d16949f72bdfbebdc623066e0696fb281504784eb`  
		Last Modified: Tue, 17 Sep 2024 23:05:28 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240911-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:343beb4436af621ada7af5ec3c6e57996ef0cd84967a8801da50564cec5368ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d705c53035dd893c37766879774dd2b71c2d517b8e0e30bcacdf89f1bf13ef8d`

```dockerfile
```

-	Layers:
	-	`sha256:53d5102f29141a507d6a748b4155e54db9106d8f13a6b0816f9df94dde35931d`  
		Last Modified: Tue, 17 Sep 2024 23:05:28 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02922166e30be974042f6fa108958fbb38fd2dcfb24c073494b070442da6a318`  
		Last Modified: Tue, 17 Sep 2024 23:05:28 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240911-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:6df67f66845fb3dfaef713053abbad0d4760503a27612fc530f8985fbd4d5bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6467289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89ec81eaf4700d97c619ab57fec4823cb6c64b9e49876452366bacc1bf20715`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_COMMIT=bc5ddc8698d56df588fd99864a650b834426ccf7
# Tue, 17 Sep 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240911
# Tue, 17 Sep 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Sep 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Sep 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ee15f27329d4d525295809554ee83cca46446076bb721774e2fb8c76110eb2`  
		Last Modified: Tue, 17 Sep 2024 22:58:52 GMT  
		Size: 3.0 MB (3005357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424d0aca809d7a575b0abb03d1f3b5283d27cd5fbec88e73c35f31c91b452ea8`  
		Last Modified: Tue, 17 Sep 2024 22:58:52 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240911-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:a56c686a9d4649cb1ea24b1d550684ba3ecbebefeaf62f18e6a69d34527f12ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c451f9e503a3f4fb44ba548b9e2625b2b7e3d0bfa991a9dc6ab6a3c80720855`

```dockerfile
```

-	Layers:
	-	`sha256:5c04bef07751999b956a24be8465ef18d96ff132add88aa5dfad20d81745af84`  
		Last Modified: Tue, 17 Sep 2024 22:58:52 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece5f4419e580057fc3d5f1e810282a32c9081976dec3ee8ba1c9118e517c15b`  
		Last Modified: Tue, 17 Sep 2024 22:58:52 GMT  
		Size: 16.2 KB (16171 bytes)  
		MIME: application/vnd.in-toto+json
