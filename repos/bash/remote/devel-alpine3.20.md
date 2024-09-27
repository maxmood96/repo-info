## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:28aa588621b190494a0f4e363b4d49e8316e47285fbe5f250171993710ac1657
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
$ docker pull bash@sha256:029886fcaf2612fc010466cbcdaa16593de7fe7c64adf8361692729feec45fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6530967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f531fad36adf29fd301371d4a4430cb4db4024dce2aa43eeed08e5288c6385c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0203390aacb422c1a2b00f81eee4a17198df3db9ba8da271a4cfcd7fa148ecb`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 2.9 MB (2906822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ffaf9a5737ac65ccc825fd1dcf091e5285d38526ac522752ff2a979dec3235`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d1facaca569c03f6d8229bee50e9f31ef59542fc39c37c416e1eaaa2acfb7f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8fda3ad341cf07dce93ee42a597947e6fb7bb21f2330b20baa9bc984063296`

```dockerfile
```

-	Layers:
	-	`sha256:731f9107aa0a2f6c8e05da516cf4ecb8cfb223a3de95c84e0bcfa1395db70c11`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 109.9 KB (109896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ef0e3f3d1c4abb9fee98302c78e8fc10e8405519fda9dd7a60987730d8f0f9`  
		Last Modified: Thu, 26 Sep 2024 22:57:17 GMT  
		Size: 16.2 KB (16197 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:27f574b3a3b49a74d59927ffd9fbdcf393aaace5fe7876db33395858798e90f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67547369362234edd7df52dda12afc13a9dd12dbaac32787407bbeca499bc3b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc73fb93c022c580235cd601a63a54b882c6b812b1886c121e0bff2e5f1232e`  
		Last Modified: Thu, 26 Sep 2024 23:28:55 GMT  
		Size: 2.9 MB (2856891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fae46bb406727a5ee16026a09bbade56a4df8d2f76a647585652600f56d19c`  
		Last Modified: Thu, 26 Sep 2024 23:28:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:308ff46a26c80c27dfb300ccd7ef0b5e513e2d4dc8fd52d49621bd0c2c2a404f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2503233bd719b875f7805fb7be3d1d6a1adcc618f93fa1123a64b84010485a0f`

```dockerfile
```

-	Layers:
	-	`sha256:9a8aea89a6288abc70037b429d127322e53cc016533c18265fe87b6874343124`  
		Last Modified: Thu, 26 Sep 2024 23:28:55 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:ed65b76b948e49497d10e9bb748cf04d222af288e891188202aa80e9bf3d4451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5894956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137bf15b1bfad29e6d9d9dcfd719b7021b9f81c9a14c4118585bca934006f03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa485c1e2b356111564da54301b94fdc7c23abef665e8110afd333d6f23ae0de`  
		Last Modified: Fri, 27 Sep 2024 07:48:00 GMT  
		Size: 2.8 MB (2799118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fd65e31cea0ce39f885aacebafa724e89f4030d8b3a6a59e490b5a33d278dd`  
		Last Modified: Fri, 27 Sep 2024 07:47:59 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:abcc68520610f0c9747d572fbc87366063fb7e2382017d459ec31ad3986dfdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c071abb4e81e187f9afc66e22eb7a529607ab1f4244ea05919a7f3c8557e5f`

```dockerfile
```

-	Layers:
	-	`sha256:b230070b084bd9b3ea8c8ed3150e6d1c3ce903194bfeb7ff5708c898f6e2c266`  
		Last Modified: Fri, 27 Sep 2024 07:48:00 GMT  
		Size: 109.9 KB (109932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08198e52cc05078edd657656e24e6c0f24c2a7513e250697be950c9c0ff1749`  
		Last Modified: Fri, 27 Sep 2024 07:47:59 GMT  
		Size: 16.3 KB (16269 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5033658a4b31aab323b88b19797e8e904d9b5dd3f19c41e4b9e156ea977fcefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7093863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce79253072b7c44688b3433e669307b3ba067889753b39b15ed7dba9c3189cfb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d304c971fccbaa3f424daa1dc072e270d798e2dfefbdd3dd148ad1d68ea25422`  
		Last Modified: Fri, 27 Sep 2024 00:58:35 GMT  
		Size: 3.0 MB (3005881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515c7faa243e7335594162b355086b475615fe58adf3baba0f600c7b39e32548`  
		Last Modified: Fri, 27 Sep 2024 00:58:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:9760d0455f83d0c4163ca75457e6478ff807d31004cfe1146e14f1b0291b245e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4986eb83524253dac880e7338196dea09afc366fadee0e3d158b0b1f976e4297`

```dockerfile
```

-	Layers:
	-	`sha256:2b71245fd866e4342b30ef2a2ff85f3b52851fcc8d5dc14c6ba9d04a7a062f7b`  
		Last Modified: Fri, 27 Sep 2024 00:58:35 GMT  
		Size: 110.0 KB (109952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7e24645467908ac6768f39f509266da11af716468fd63397fa023a1cf366ac`  
		Last Modified: Fri, 27 Sep 2024 00:58:35 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:094c35cb38260ab03af4d89427d843548fc5158f450715bcbdd97d3042e79d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614d1bf8eb3b5badb5dcc6197aae4216034e23cefafd371ff84324207a62194e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b349bbae4cdbacfdd0de144d99deebac8ffc6c2bd9347b26ba35b2b8be3d29`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 2.8 MB (2848722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1627a815657b639de64d773698a942fc0d64707cda76a671255af245eb2e0dea`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:60c25f16a728213606a1a1ab9f2065e3c589f8f3f44ff2c9e5931136722f683d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d90a65866080d464acd6ccbf101b23a562c201be9effd9dc70efbbc9899cbf`

```dockerfile
```

-	Layers:
	-	`sha256:a631a36772d67c9a63abc801f13bca96f8c97d9dee07c024fadb4683647c4aed`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 109.9 KB (109871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7717bb7f76b3312369d7cb435c39f04463b520446fec7f23c2e913ca5f74eaec`  
		Last Modified: Thu, 26 Sep 2024 22:57:19 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:8bd70e5cd67f77acbb44395fa4c882d205c271a52c4ef6deb62253b13ce3cce7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6752377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd5a6474b896ff34f5595e76a31bd9303e7dc730308f81b2a9b18843fae465a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351673906ef65cf36ad4e3fdfac978d6dc670894fa38cceae1d19d55c46b32c3`  
		Last Modified: Fri, 27 Sep 2024 01:10:27 GMT  
		Size: 3.2 MB (3179621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74c619ce3e1846603338bd6e876dce3bf9cd9b8260df44538015c1264831ed5`  
		Last Modified: Fri, 27 Sep 2024 01:10:26 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:a8913031410661bc037b23d742ec37627c351d464c52d256cc3d6d7db725f18f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7ddcc430d7610a8dd0097020bec62c040c2fc813fbc1245351541315d417f2`

```dockerfile
```

-	Layers:
	-	`sha256:e8c765667a91ce9d6fb01b4f86f08d20cd8d34691741e2b5e7716b7f2d7ca4ef`  
		Last Modified: Fri, 27 Sep 2024 01:10:26 GMT  
		Size: 108.0 KB (107976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f774167faeb717b80f619bc08d8742d6d882ee147e9c5df9e05d52d96258526a`  
		Last Modified: Fri, 27 Sep 2024 01:10:26 GMT  
		Size: 16.2 KB (16237 bytes)  
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
$ docker pull bash@sha256:41e26dbc30a368dea4552cbd6bb86c9e6be70f674c9ee6f1ecc9d95f8f4870e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6467508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff34e6151375183e12e3ce100d4dd6e94468a61f85350e1a0d5dd0ce75543bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_COMMIT=8d74195d7f379c6adaee217f50d60d0c8f79ad8c
# Tue, 24 Sep 2024 04:18:18 GMT
ENV _BASH_VERSION=devel-20240920
# Tue, 24 Sep 2024 04:18:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Sep 2024 04:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Sep 2024 04:18:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e866abf193e6e8dc2569018b8d434b607341a1721c3d046867f730af6a8c3b`  
		Last Modified: Fri, 27 Sep 2024 00:33:20 GMT  
		Size: 3.0 MB (3005575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43c5f53911cb0fd44d75b15cf1f909a62157052f5e401a83fd45d551ac0c0ee`  
		Last Modified: Fri, 27 Sep 2024 00:33:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:ee2300f9ff619d13bd26f2e51d39f370c7f10a64b84ec8cf3c896fa41a0b1312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870abb71eed3eac9e7f180c3d9e711ccb2961aecd5cb1e045b95c2741f8e85c9`

```dockerfile
```

-	Layers:
	-	`sha256:10d086280d9a2b212e9a752538d2eb282225300fb95a9adb72a803b1936cadd0`  
		Last Modified: Fri, 27 Sep 2024 00:33:19 GMT  
		Size: 107.9 KB (107942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225028c8d14f4fd3d29af4a6a5f5b4083642a3f498ce6f92576b781a5b58b3e3`  
		Last Modified: Fri, 27 Sep 2024 00:33:20 GMT  
		Size: 16.2 KB (16199 bytes)  
		MIME: application/vnd.in-toto+json
