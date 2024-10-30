## `bash:devel-20241028-alpine3.20`

```console
$ docker pull bash@sha256:53c08552f488f90ed5aa272a3bc83c1fa248dd2437d90d4ad8d7c5041cab2b81
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

### `bash:devel-20241028-alpine3.20` - linux; amd64

```console
$ docker pull bash@sha256:3a00b26b86e2313d901c6449e47359b89b476387c170fab5842453809084ff11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6537512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69e47731ade6f38ab4ad6b04f33bc658660de7984f7ba3d5a6322931334ed7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e36191f6061cb5fdb1b4a50d2bfbeefa0477bb993537e9f0a1e61a9ff389a8`  
		Last Modified: Tue, 29 Oct 2024 23:03:31 GMT  
		Size: 2.9 MB (2913372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd81d8f22ed837f73858373d1d337a3fedda567257b70e3df8d08abdeb7f280e`  
		Last Modified: Tue, 29 Oct 2024 23:03:30 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d2b20c834bc4c89c02184975631bf82ecac2223ee8759605d37cd6e06c2bba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf63a71a36f21282a80db0071a018390897c494067f7282c7d88705836a532`

```dockerfile
```

-	Layers:
	-	`sha256:4726e68cdd32861c2477da5ce6624520435752a2514737625986524ec9d975c0`  
		Last Modified: Tue, 29 Oct 2024 23:03:30 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130fdab5c7f35b93cdf0bc089187ceee14c203929ac1b8fb5a29c0a1c8eb3556`  
		Last Modified: Tue, 29 Oct 2024 23:03:30 GMT  
		Size: 16.3 KB (16333 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:d118eee4029ed9ce92dea255e4544ee92908c103bcde15eb187cd383098b43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eed3535483fb648516f4a80dc374e0303f6761a04f4b7cc6193ccc1472f5a3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2d11791fda95334c7a206d39be2553e04813ea5efa6cea50cc2bcb36ae039a`  
		Last Modified: Wed, 30 Oct 2024 00:53:20 GMT  
		Size: 2.9 MB (2858502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c292f567e757ab65dd02496f9c49a89b33d0c4bcc0398ff1961f6e4e1b8c0a4`  
		Last Modified: Wed, 30 Oct 2024 00:53:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:eec1897eeeb7e741637c3a077387b9d3e5c291daf10e2043eeb93c866ec52bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9304efed45df3ef8cda199e6cb71272615772323fb3a9720878077ed463139`

```dockerfile
```

-	Layers:
	-	`sha256:febcc4e88cc40deb76547bca0ee509dfd2cacc0d2ce52e965518a23f3e2536f9`  
		Last Modified: Wed, 30 Oct 2024 00:53:19 GMT  
		Size: 16.2 KB (16188 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:6ece950a7a1593f4783a580c5419a7951275f8b31fe54012dea15d2d3e9a8964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54904b5df14c5e0f09ed7382d47ffb0d14c1d9e0f31cbcdd0e44cd35e9bc541`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae7e32757749a9e9939b0e987883321053a092faf916955b5089dbd92e92b35`  
		Last Modified: Wed, 30 Oct 2024 01:01:28 GMT  
		Size: 2.8 MB (2803370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bcdfce302c1b3efede76365d3b653a969adcbf31b001a0edcf3659b55cbfcf`  
		Last Modified: Wed, 30 Oct 2024 01:01:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f4cd46860a6bd9fa26248d903996480933b9b46b655175be749fe71540cda096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa92308d6a6bbcc2affa6387bd8a809502f4f34d7a362966ece6d83340ec8fcb`

```dockerfile
```

-	Layers:
	-	`sha256:3655c919b107bf5032decee7e0c912f0f473177281d0c3ad7e56139aa5a912b6`  
		Last Modified: Wed, 30 Oct 2024 01:01:27 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222d3d8ad44ae890b19c29eef57910a0d1f097ab9ad4da481226b5ccdbddce27`  
		Last Modified: Wed, 30 Oct 2024 01:01:27 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b8bdd0e34f2a3a64eb77305da1b3aa41629727e4d12aba93cb7e8758e5dfb855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7097315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fa694b9e91811cdb96aa6cf48f2c011d40b075eaa28271a72fa33110320004`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433520eebd9bd2d49ecc64114584a9e16039827415dba9673e1f35d3b6153d21`  
		Last Modified: Wed, 30 Oct 2024 00:01:58 GMT  
		Size: 3.0 MB (3009338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00588760bc4c0212d6e7ecbff88ea632ce2278cde6e14b7ecefdbedfdf6c7fb4`  
		Last Modified: Wed, 30 Oct 2024 00:01:58 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8b889ab6177f84fa5e8e6f924d2f3cd63c7c8cbb5c646a06ab5363c34e214f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd8d47a9a50420cdabd7b5b91f961eadf1acbb79c193ac6dcd4a4e267e771a7`

```dockerfile
```

-	Layers:
	-	`sha256:9dd5d33fb79d6e7c7a30041249458d1c2540432907577b953a637d362170e723`  
		Last Modified: Wed, 30 Oct 2024 00:01:58 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b438808db6db93e98f54a6ea6da35366f155c89f8edff6af67537e925bea1911`  
		Last Modified: Wed, 30 Oct 2024 00:01:58 GMT  
		Size: 16.4 KB (16431 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:1f7570d66277b52c62569508dc57c2c04c138eff71653366d5f13ba5a10df93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6319841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd76bf7dfd18f052c3e44c8e6f1930fa4e6ca0d89f44e0d5ae9bec1dfab1fdf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2355cf00abb946d64a6359205ef4b57217f583a1cbab89b588fc681a23e06`  
		Last Modified: Tue, 29 Oct 2024 22:59:11 GMT  
		Size: 2.9 MB (2850337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adcd76e1ae33601d23a6ec26a405ff248ccd8e6cfb463320dd72f06a74a2cb5`  
		Last Modified: Tue, 29 Oct 2024 22:59:11 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:372130dc02ca40a806751cb8278bc944c28b0d947dcf0fd586f1e6dca94de455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9548170287d925187acfe860f274276f3fb2fbf0f42864092a9050a77fd27a`

```dockerfile
```

-	Layers:
	-	`sha256:d9fc43746625d7556134a3737f73ab50fb3bc48296649f1422a5cd511a0d76bf`  
		Last Modified: Tue, 29 Oct 2024 22:59:11 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c307f892464e46bd1bcd932e4e431d3324c26ecc4fe30aed89e5efec5dd2e3`  
		Last Modified: Tue, 29 Oct 2024 22:59:11 GMT  
		Size: 16.3 KB (16304 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:06c49a764211b4226c051d5488a5cfba4dd94fbf56f314b15b4ed936b79caf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6753957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ddaa7e37845c7889a4fe28f256f62534a0be161df1da2acbbb9e46f97ff717`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a359a087bde19500be8a4c90f2d10554b8e8821b1cc31f3a9d7a7a94a26c4cb`  
		Last Modified: Tue, 29 Oct 2024 22:59:06 GMT  
		Size: 3.2 MB (3181207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfc16d8c30457e5f6cff32429456aeeacba4fb77787d6b7cae05037f496be0d`  
		Last Modified: Tue, 29 Oct 2024 22:59:05 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:a32bce2ff9ba2688aa79b3cef6df0b23173a4d67639f150e8cd3e9f474685e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7827783282b916fa3ccd2df9e57397968fbc35782bd3f7dd9b8fba86a4e7b518`

```dockerfile
```

-	Layers:
	-	`sha256:96b3211864dad7ce9001a575f9647334cc3937dab657e33f34fe0fe2a1aab8db`  
		Last Modified: Tue, 29 Oct 2024 22:59:05 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aabd2c317dd613d694e402325bf39eb4b4af9fb3c34aa4e8292555e8671e3eb`  
		Last Modified: Tue, 29 Oct 2024 22:59:05 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:6ac36ca2fb0ca55ab2bc27caa24341f1621183e513bddcecf6019087d6b54286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc98094880425edfabbace077806f49e509405f9f9cb225c8c8965f948338b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c158982915ee442814e845c49e91020837341df4e5e47bed40ee4055910526e0`  
		Last Modified: Tue, 29 Oct 2024 23:05:26 GMT  
		Size: 2.9 MB (2858474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0eaa8dc467c9f1e9ef7ae62fb6e3c753a95d8ec2c7a8e59d65714bca72985`  
		Last Modified: Tue, 29 Oct 2024 23:05:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:a1bdc614edbfecebfe7cf0bda311135d1c9436611d0dd9a7aa3b29e9ec91d39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb6e3610ab59ae716186cd6fdaf5a5711be5604a4f42da3df16ed4ff7294a31`

```dockerfile
```

-	Layers:
	-	`sha256:a3032eb41f5d038b17a75e9bcc0e78e740148096df7f9b77a2f6292bae27c9f1`  
		Last Modified: Tue, 29 Oct 2024 23:05:26 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6ab86730f28768a013bc51f91b058f283d9b26bcd4d07076a68c60ab5ef8a0`  
		Last Modified: Tue, 29 Oct 2024 23:05:25 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241028-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:5e61903c5914adfbaf9b50d5807daf61d3c219cc052282eeed0584447e9a7375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5ebd8b4c57e32e98e2e1bbf23a8eac7501500bf545c112c0529e0c7caec02e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_COMMIT=4917f2859c8624e834f589bbd526a7b707072ce3
# Tue, 29 Oct 2024 04:18:14 GMT
ENV _BASH_VERSION=devel-20241028
# Tue, 29 Oct 2024 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 29 Oct 2024 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Oct 2024 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ab2ad82d5ba31096cf6f44d840fcf7ab16361857801423bc99702084f5b66e`  
		Last Modified: Wed, 30 Oct 2024 00:26:42 GMT  
		Size: 3.0 MB (3010059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc433f49d84569e2a6a78ab1ab143ad513ce5fbb0c8bb9eb893e784195823f8`  
		Last Modified: Wed, 30 Oct 2024 00:26:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241028-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:9817cead79552e7f66bfed3df4ec27dbf43f35f9232e0ae6d8e5f8f4bd54a79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74546678d95a5ca1a47f47424656b393a691f1e619b8468083626e141793f104`

```dockerfile
```

-	Layers:
	-	`sha256:76117e59e7dbc863879b75d4a7683faa5b641016545629903b1e1fa25b511fe8`  
		Last Modified: Wed, 30 Oct 2024 00:26:42 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3786fde512dd375f4668833bafff89816331fff683f377e5f6dd25ae159037`  
		Last Modified: Wed, 30 Oct 2024 00:26:41 GMT  
		Size: 16.3 KB (16333 bytes)  
		MIME: application/vnd.in-toto+json
