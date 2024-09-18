## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:a56e0e79dfa8651b7c3e41b5e20c2a1c835d79236a0f1ecd8b3b2240b024dbcd
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

### `bash:devel-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:6e893a62dc0340a277c2e9be7d5e7c2286b18c1d87e3abbbd4de401211cc70d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6529916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc1f6de65ea06ba90edba13b08275a56c94f7893206b63c160eba7b5f5311be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_COMMIT=5576c26da8e0ad74048203398acb493c65fd3476
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_VERSION=devel-20240904
# Tue, 10 Sep 2024 04:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b7e33eac9c47f719bfa8107e5ded940e6e35a32b2bf220ce830913a713ac7f`  
		Last Modified: Tue, 10 Sep 2024 23:59:45 GMT  
		Size: 2.9 MB (2905773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603cccf1f8d540f5f7e7074619c2b0bf46540b48e64199e7bd9ea9aee97f5dd6`  
		Last Modified: Tue, 10 Sep 2024 23:59:45 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:103d1eeb401ff86871bdf1c82f1c1788e0b482011a404abeca1f9aca249d4dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ec2deaf2871fedf263fd9e68ddd7c7e2b63aedfc5088d81d089eebb9b4e12`

```dockerfile
```

-	Layers:
	-	`sha256:b353b419bf22e99621d9ffd40767a244e4058e56d0158fd5494e7f13ee18df7e`  
		Last Modified: Tue, 10 Sep 2024 23:59:45 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e9285cdf8ae954094136c2005a870d29810e1ca0c860692ce0276591498590`  
		Last Modified: Tue, 10 Sep 2024 23:59:45 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:ac6fb6b6c92d244fd5c398ff3bcc062e0ee31f0b0f4af5ca2047c20cfa36a525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5121b2a1a25f0c943cd48003211557bfeb5d9dc6d84c7044d2ca269e37ed4ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_COMMIT=5576c26da8e0ad74048203398acb493c65fd3476
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_VERSION=devel-20240904
# Tue, 10 Sep 2024 04:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a2e4a4ea8d1337e03eefc3abc391aed1e1985341dce353ef05f5522212b7ea`  
		Last Modified: Tue, 10 Sep 2024 23:59:41 GMT  
		Size: 2.9 MB (2855695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380fb5222fdd5a743151b2e603d4042ec304d76795feaa96f36f2587eedd26a0`  
		Last Modified: Tue, 10 Sep 2024 23:59:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:eebb09a99b3c93476a1b8882eaecca91f4fcfe5b962733cf0928e428c306ba9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8695ca82f07e56619e9c7eddc182b59ffc7409418e69ca7f51f8f51949c44a92`

```dockerfile
```

-	Layers:
	-	`sha256:1d1afdd6b176546d3cbafb8fe398938c15be262d8c9b1930ddfc831cf0b68872`  
		Last Modified: Tue, 10 Sep 2024 23:59:40 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:05c8e2b63c61e41629179db9f52f5fcd2b5a8b18363f7fcac66c5eea3844572e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7092935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31dc798f06dd1af9142ab09cd531f8653c0fbaa89ce8ae628e4f06344e2dc85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_COMMIT=5576c26da8e0ad74048203398acb493c65fd3476
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_VERSION=devel-20240904
# Tue, 10 Sep 2024 04:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eaa4db574fd3292b6ecdf83a1b73eb4d4a44056983d54abf45da0a64f7a32c5`  
		Last Modified: Tue, 10 Sep 2024 23:59:00 GMT  
		Size: 3.0 MB (3004953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd280a820b70223ee81f8e511fee050d417b5190a276f5aea57a90a3f0c89fe4`  
		Last Modified: Tue, 10 Sep 2024 23:58:59 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:bf4c3f277a60051ea4f3ba247578973b55c29dc5e28d71f4b9cded049245b2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2c87b77c46872567812acdf9ac10307868612ac9d141c5110aa91d93046048`

```dockerfile
```

-	Layers:
	-	`sha256:208fa2911970a67ff685561b750755775ed8065e8a3fd160862d8d19d5c54bbc`  
		Last Modified: Tue, 10 Sep 2024 23:58:59 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ac4c6b042c7065f1a9f00c5854305b1a449eb460aab0d61fa408820c5b5d534`  
		Last Modified: Tue, 10 Sep 2024 23:58:59 GMT  
		Size: 16.5 KB (16506 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:55d6171c17e1c584f2ea4c6eefdf47f4b2abb002355d82c1b4973c12c64f4df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6751478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e6681131e128693faaac97a5a31cccd2513e4d1f183d731fa8ef1b2901c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_COMMIT=5576c26da8e0ad74048203398acb493c65fd3476
# Tue, 10 Sep 2024 04:17:51 GMT
ENV _BASH_VERSION=devel-20240904
# Tue, 10 Sep 2024 04:17:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Sep 2024 04:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Sep 2024 04:17:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a99285d802d2c0720c1760a7c318d4c7a6b44a56d695bd5539f3759a8f0ca0`  
		Last Modified: Tue, 10 Sep 2024 23:59:09 GMT  
		Size: 3.2 MB (3178723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de04a73fda6555e1ffec9c2ea31639ecbc6074fe84536cb20f329766c05796a2`  
		Last Modified: Tue, 10 Sep 2024 23:59:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:fe16b87f047da014d62db3f8e71c6ca062e358f1ae2564ae94335903c9f960ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ca24e70d44be52d0c67b823cf4f47d0507688715bcaf0ffed6422debaf6b56`

```dockerfile
```

-	Layers:
	-	`sha256:f2e746164701bdeef9fa35b7bf0b179693791c2d1916de9d7758d6a31e229c31`  
		Last Modified: Tue, 10 Sep 2024 23:59:09 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69fa9fbb629c931efe693c3652460bd7d18c2bfa39b72d03a19b00442fee60b0`  
		Last Modified: Tue, 10 Sep 2024 23:59:09 GMT  
		Size: 16.2 KB (16245 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; riscv64

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

### `bash:devel-alpine3.20` - unknown; unknown

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

### `bash:devel-alpine3.20` - linux; s390x

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

### `bash:devel-alpine3.20` - unknown; unknown

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
