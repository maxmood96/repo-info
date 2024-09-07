## `bash:devel`

```console
$ docker pull bash@sha256:2c418b3ecac6153494edd69f8da89b06bcdfb73f9407786fc6a590f5052ec8d0
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
$ docker pull bash@sha256:329d0f4023a37e5722594163b3f2e0d836464fe5b07044dd239632b72bcb3651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6529301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8762fec2b574a37c23e6297d9c6ecc9d2539dd97c9b6106c14670edc17945ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c434997d797e740b6332dc4d53506681248fee6dba660321ffc05bc6a332b0f`  
		Last Modified: Fri, 06 Sep 2024 23:15:42 GMT  
		Size: 2.9 MB (2905164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae697dc373db89b0dd9c651b829c2b56757a64a36dace44751681041a515afdd`  
		Last Modified: Fri, 06 Sep 2024 23:15:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:17d42e7ed43330705d72c8f3b571527a1a2043c78960ae2c6cf69e4264b11bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af9b5ff55892d0cd12a053bea81fd9c17a04d82f6a5593da6b779a699722f71`

```dockerfile
```

-	Layers:
	-	`sha256:5f7762c76b45ec494a246443f7c344bf061f208a31959018364559284929cff9`  
		Last Modified: Fri, 06 Sep 2024 23:15:42 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd163485ce3cad72ee4a3feca8e7922d76427a2c9123929fe506ae5029461a83`  
		Last Modified: Fri, 06 Sep 2024 23:15:42 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:8f327644961360ba6b9094f77137d9d3bc1769005b2c21eeb165e49d55814fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6222144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ce6fa68b49981abb8031a5e35b8f1279c908a6cd060b593fd8c656bcf8ae20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cbf537d1b9212bd45aa55b0182c7067a919943e430426f48de230ab1f50c6`  
		Last Modified: Sat, 07 Sep 2024 00:57:20 GMT  
		Size: 2.9 MB (2855303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c58d7b574a0532ad072bbc2e4004c5240e81518f21188b70f48b9b2ae0e1a0`  
		Last Modified: Sat, 07 Sep 2024 00:57:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ff4080b577c036869d234bd8932762d6b5be176f90b931c09d44f28e632a8544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5430515464a01e1fb580741388e1b8a3abe464a0d9fb08470a807ba35105cf68`

```dockerfile
```

-	Layers:
	-	`sha256:9f294bf17ff0a7e87859f16504c7ae8b9d191775b8fd83f6e7971217d17b5323`  
		Last Modified: Sat, 07 Sep 2024 00:57:19 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:cf867840339ec1dbc1c17dd5f38a150ad8b6fe74d5bf6a655809bd4eab4145f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5893858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324753d4d9f149ce5912e5c8287add17f4072c9a0f3508612d64195add81ec8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b693bd7852d92a85908da03158ae571ccdb169fc1c0f75317333d391e84df`  
		Last Modified: Sat, 07 Sep 2024 00:07:53 GMT  
		Size: 2.8 MB (2798021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e703c367317c3c91eeb14f29890b5c33356109126f032737af6f7b6832bf23`  
		Last Modified: Sat, 07 Sep 2024 00:07:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:746e2148633ba496c0a706aa1636f00dfa7388d560f8367544b302d1b0e2a55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5ba3889cd6a3d35c81a6ded71712477a87e1ce7d3eeaa1419eb095069add2f`

```dockerfile
```

-	Layers:
	-	`sha256:1fab3ea7ef2599b35b0ac28920815673377784601df06baedaed2c7303f8c515`  
		Last Modified: Sat, 07 Sep 2024 00:07:53 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fbe3f514d857420c915d92f7d207a81cb5b1eee27475c27fc1d7367dd4ff37`  
		Last Modified: Sat, 07 Sep 2024 00:07:53 GMT  
		Size: 16.3 KB (16277 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:348b92151ec3851a85f2767e8b01de03ec43c883d413c7c12ec9ab7821373cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7091543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e55af8d664fe38213e56ce1d6837896251a70070867bbea478da01c4a07919`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016351f45dfb77ee22922a678ec437f6f11c140dee86ff41e6da73421400c01d`  
		Last Modified: Wed, 04 Sep 2024 21:57:28 GMT  
		Size: 3.0 MB (3004276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3855cf3c2b39b603643c1e65d0ddff25afa5d6aa95766a37634d220be4dda07`  
		Last Modified: Wed, 04 Sep 2024 21:57:27 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:736ebbe1d68fb6d5812fbc941dddac818dfdf8507d0f07c3b4f39343f7774187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ada9b2d9e367e7fa52e931ea5eef5e7321f2a6f7cdc311b95c5f0f716bd9669`

```dockerfile
```

-	Layers:
	-	`sha256:c477e3237c1bae1bef3f9db1d12e03f307305494c020be6d26356c29446c34de`  
		Last Modified: Wed, 04 Sep 2024 21:57:28 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8954a20659bbf21bd39d42cabd886701c122fe3cdcaadccf0ed951614cabd35a`  
		Last Modified: Wed, 04 Sep 2024 21:57:27 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:5fb20a7b4f5c34d6499664f76979e0a726a5a97322ce54a25decac861b5c270a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6317393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0500e58ef6c0f78adc1eef7d91bd36311ed0f8b1be523f4a8c7acf391d4fb56a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5994a25ea4c86772f1e5c67e443616ed58bc596f517322bbbe30af016eb13832`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 2.8 MB (2847893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a165e3dfb78ba3edf3541ecc11263977b30afabf642d2e71256f6e226bf7234b`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:dd55c8e230e5ab4c001e2193a8c3aeb05fe68ca59d5e7fceab59a8a660a8d0dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf7c4c6a7fe2e4384e16c5b59f1e9eb38aaf84e14468d67486316126f0020b6`

```dockerfile
```

-	Layers:
	-	`sha256:9da11d5b84a6a72416c3f7d93142a0ec955372dc33e5aee8b73cb6d3c065cc15`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd84b22cbb258070f905cd6bb5a9e81f782879457da17c10a6ca38466c08a4`  
		Last Modified: Fri, 06 Sep 2024 23:15:45 GMT  
		Size: 16.2 KB (16176 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:f1a27fe7c325c8d1f6e2e6bc1bc5d1f9162622842e02b46a886bd7c43f89c59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6751191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b2e40e4a0d2e7e7beebabb97e2f232d79a4d330e89067560630d161ef9ffb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb99afa71ac42915897562cc64d15ebfdbbdc731b3739781239d7fde6773b7`  
		Last Modified: Sat, 07 Sep 2024 02:12:04 GMT  
		Size: 3.2 MB (3178436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ddb4ee4b553be0eac2ca9d68feb9a61a21f38609faa447bb541872ddb60005`  
		Last Modified: Sat, 07 Sep 2024 02:12:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e3d50b2eea6ff220a34c93a7bdf1767815fbaf29288ee1ee8ec7522dd9d4990d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37b3d9900d9cb90e46d0015ed80bb6960aa021a059ae8ff3e4703b96e5d1095`

```dockerfile
```

-	Layers:
	-	`sha256:3032d2b168ad1ccddc687b8ba5af96e77bd834ae7a83ce7bc6853bf452dbefc6`  
		Last Modified: Sat, 07 Sep 2024 02:12:04 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860e521c411515cbc049d5d818e405ec31f7bb89868ef9cbabe158e31c92accc`  
		Last Modified: Sat, 07 Sep 2024 02:12:03 GMT  
		Size: 16.2 KB (16245 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:29521e8418bbd8f554399c6865b02dc588aec4293ba4447296cd02887df78e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0067fc79c0811e3a1db3abd69b5a890e51168c57582a7b49fbf12958ea5dac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf29773fa21477cee4a300065d1ec47dedee923f40ba2f2797f4b45249f7a26`  
		Last Modified: Wed, 04 Sep 2024 22:04:04 GMT  
		Size: 2.9 MB (2855599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5a0b824b157c026c3125675edfec8ec0fc4c48cb053f2d93b6adbc3e99c984`  
		Last Modified: Wed, 04 Sep 2024 22:04:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e0b384f083523f5dfc8cdd9d1e6b188434315ca3e3075d72b50da168a793c8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8280f8e40910b8162c14678e31af207433235dd6889ee9b4af9c9b1dde5a8d4b`

```dockerfile
```

-	Layers:
	-	`sha256:7e97be6ee25d05b34238921adefaee54a2c8b55714ef5757d2a1763f4aff285c`  
		Last Modified: Wed, 04 Sep 2024 22:04:04 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c50605c5a3026875160f7ff1221de6c7a19c0129b048bfcda45380b25d435fd`  
		Last Modified: Wed, 04 Sep 2024 22:04:03 GMT  
		Size: 16.2 KB (16245 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:aa8a7e455fd629aaaa0aa35943d79a9292c2fbdf3004c1677b18377186831311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3239f5a6846e799670422cf458139d8939286b6ae52f44b4af454cb8b5c0da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Sep 2024 04:18:04 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_COMMIT=2610d40b32301cd7256bf1dfc49c9f8bfe0dcd53
# Tue, 03 Sep 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240828
# Tue, 03 Sep 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b73e72769b118ab313cd0223bb3181144dcff30c19deaec7d755e0c6eec6a1f`  
		Last Modified: Sat, 07 Sep 2024 01:02:45 GMT  
		Size: 3.0 MB (3004817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb28b43768b5f93255a49d39628a6e81925079d8fb8ab262bdf47e175cd8f84`  
		Last Modified: Sat, 07 Sep 2024 01:02:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a1fc8fc6d6c245f8db6726628d6a562058ba4a90fb025c3e12897d78640fa553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade0b76886e956bb75004e9f20dcd1b5ee5295d1fe46ab80a0ed326a5d5ea698`

```dockerfile
```

-	Layers:
	-	`sha256:93aed7af38a379ff32abc117a569e303c8849f3fa5f1e1ec60487ddc3c64f9be`  
		Last Modified: Sat, 07 Sep 2024 01:02:45 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fab9bf165373c0caebcc3cdc7ffc23c990ae788143fa22be11ea2ceeb362931`  
		Last Modified: Sat, 07 Sep 2024 01:02:45 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json
