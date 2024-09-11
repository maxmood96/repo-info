## `bash:devel`

```console
$ docker pull bash@sha256:bc14e65ad700aaf21e229f799a5cd0b71c4ed1e558ee0785cc38bf975e4eccf1
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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; arm variant v6

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:bc7fcb38f5a143a72d8a06c33135719aa7c5284741448d7a36c7a2316f7fd9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5893571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4939c099ec904fa4989fd5ac59e867f8de91afa3199957d5257624e79ecf49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02e5b728ad3e9110e2ee7a9c102b30e2449f50bfc9fa2dce6ad9edef72f81ea`  
		Last Modified: Tue, 10 Sep 2024 23:59:55 GMT  
		Size: 2.8 MB (2797737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1dc6d9288b5785f1e10d7829467655a530e59f7cd940b73da27a4fa3f9956b`  
		Last Modified: Tue, 10 Sep 2024 23:59:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a57b231e992ced2ee6651b06b0ef1721e114701a718823ec3219e7576dbc4cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554d667a5adbdf52ceea84ec9983c790816657c3078e2282af7d9a1835789dc0`

```dockerfile
```

-	Layers:
	-	`sha256:98a2286c6fefb7b06eacf94404b99b31daf41645654e8ff043feb83f9df33823`  
		Last Modified: Tue, 10 Sep 2024 23:59:55 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cacf530c43c98d995caedb145d38f8aa6c6d5fef33ad96ddd109697ab355022`  
		Last Modified: Tue, 10 Sep 2024 23:59:54 GMT  
		Size: 16.3 KB (16277 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:c9d3e73303c0309d0d180ea97953bfa7faf5e1e6e5d965bb776a0084f50468aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6317507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5960d17b50aaed2cbf2f3d04732ad4e31070311efaa39d1ede743921620b1f8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cfbbbd7309bcb9437e20485e0462e3ef5777a5f239610e704324cf794849fe`  
		Last Modified: Tue, 10 Sep 2024 23:59:10 GMT  
		Size: 2.8 MB (2848005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9fe4fe84917d7581d99f585f76b8572226d3ce6f0ffac404fc39555dce6aab`  
		Last Modified: Tue, 10 Sep 2024 23:59:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:817760ab208af9ba35127a1caa3a4f028ed8353f2c6c5df6fce59b1faa298eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3c39a7a6adb9f6c3db47c22d602dc5be91127a5c34b234776e40f242b72756`

```dockerfile
```

-	Layers:
	-	`sha256:3c252ee1724719c37e516d5f0d750c1a2a1523936cf292d61ea589d7b7eaf2e5`  
		Last Modified: Tue, 10 Sep 2024 23:59:10 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d11eac6d0338abf86004a2044637bae84d3c0bf73c247cf3eb37728506d18082`  
		Last Modified: Tue, 10 Sep 2024 23:59:10 GMT  
		Size: 16.2 KB (16178 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:4000d82c4f9050b4139cf45458630f19145ed0c84d6489edeabb0806badeb094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6227403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685d19d8566d3ff604b64d9a424859b225f0c2d82a149b7f3ef29a0b6168cdf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df42f8192db0a4f8072972eed80413605f36a57003742a57e9058f146d07f7ed`  
		Last Modified: Wed, 11 Sep 2024 00:05:36 GMT  
		Size: 2.9 MB (2855613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e05f4848b93f16801f7b91d9a51ec720351f2fad24679a99fb7fc84aa2ee27`  
		Last Modified: Wed, 11 Sep 2024 00:05:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7d4c951135d168015e6ab30dc235b70b6a45641c62f8af66d4f97d8bc86b5377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b59ef1aea2bca30975b6bd8ae20f6f96f084538ae89761f0bf42b61f145a409`

```dockerfile
```

-	Layers:
	-	`sha256:e4eacba7e4d2dc8f99d09205a6f6ccc3b1b0fc650fdcbc30811902c753d9b721`  
		Last Modified: Wed, 11 Sep 2024 00:05:35 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ea824cd4317b9bb4bfc90d8d1aac135f629c06930770ba8d95121303f0c1e80`  
		Last Modified: Wed, 11 Sep 2024 00:05:35 GMT  
		Size: 16.2 KB (16245 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:d6908ffe48b3eee36510c1385575ba0c90b542d5858fea261c48e701365609c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6467011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313061fe32d3d3b4927c10260d4bf5ddb76db24e7bc88e6eb90433d3a7a7fd3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc923697d1c4d3dbc2038b2b920e248c7cf9fa3c605c8094e13315e8036c62ef`  
		Last Modified: Tue, 10 Sep 2024 23:59:00 GMT  
		Size: 3.0 MB (3005081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2dd7ba7e583abdc25212db4b3d3d45184f256cc81c5e3151625de4d788cb323`  
		Last Modified: Tue, 10 Sep 2024 23:59:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:44d107e33c19ea746882f7cb42c5997bdddc5779e90712a0196b40b5b3db3201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e50cf6bc5e788060004f6f311cab2b5d727e515b833da7b04103dc1360c7f6`

```dockerfile
```

-	Layers:
	-	`sha256:17d01058457e2a669d2c523de2eb2b04fed5ff3638f4d049ebaf8184d91cccfb`  
		Last Modified: Tue, 10 Sep 2024 23:59:00 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4019f764e559e0a68a25ed90f2fd34a4e53794230297be00fa5efa71f079461a`  
		Last Modified: Tue, 10 Sep 2024 23:59:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json
