## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:889b90f7c1946e112e157adcafa7fa0157a1d8caabf9273aab09816fecccb396
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
$ docker pull bash@sha256:6e46880f84168b2e04f5d58469e0475c4b37636c544ee7cc1407660488106559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6300871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aba8b56ccd33e3332cfe034d90cbf1e7b637ab57787d3abf11264cf75f61ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cc740a4eb7b4979c93be778694dc262191b4b225287c5bb1fc064fff19610e`  
		Last Modified: Tue, 07 May 2024 21:52:02 GMT  
		Size: 2.9 MB (2891806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821a1209f2335ef26b7e0349405567a1da71eb33be03068ff7771f5716203f0`  
		Last Modified: Tue, 07 May 2024 21:52:02 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:feabecfb39712ad9e1d760131d6d402ae128ae2eab81feaec5f86e25ccddcc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56ef6d2f59baadac2466a0d38533e00e7fe23304e4337eced86de6ee57d108`

```dockerfile
```

-	Layers:
	-	`sha256:2891cf80386b658b74157480ec89c5566d953be29c3b0a55e5d26a65a2fa6f6d`  
		Last Modified: Tue, 07 May 2024 21:52:02 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da953b6313141734bbc34ae78b8a09814e9856b9405dda8013da3b54b1aee53d`  
		Last Modified: Tue, 07 May 2024 21:52:02 GMT  
		Size: 16.3 KB (16300 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:ee56d438dcc4206e663d4617c8535df8fbc58c5f54ca30eacff2137278beed01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb85a5d9b6b18587fdc37d4fdb1a63d0de953de88fc5d7a4374c86bcf13a7b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a4df1b7769ed16bae852376ec8b7499accf5a9f5eda78bd3039f53033de70f`  
		Last Modified: Tue, 07 May 2024 22:25:39 GMT  
		Size: 2.8 MB (2842872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094547b7c247001d9c20754ef24541d6a9c217bc53f86010d1aa90d87986c29b`  
		Last Modified: Tue, 07 May 2024 22:25:39 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:027c563e4babc5fe5e498f7a6785d23198151056cd99abd7dbcedf0291b0a285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60cc2022a449e704a57dfc0077457afb8e176f511d58168959dd55053404afb`

```dockerfile
```

-	Layers:
	-	`sha256:b4c8addf13fbde62490cdbf45042ff45ec52070ea053cd25c05a7d34b85422b8`  
		Last Modified: Tue, 07 May 2024 22:25:39 GMT  
		Size: 16.2 KB (16151 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:13cdfefb4551f40a64a9ae0484b116b2f10147b7b0db28a5f7e2c4e27e371408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5706300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06124d1280fe695ba438e3adf184dd4cd256466491708c72c4a768b59f9c4959`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce5494d5b7d01c619a2e3772895237d5f08d8684b676a16f8ee4fc90c8abd9`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 2.8 MB (2787069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e14b1601786af4e4699135206cb28bc06d99e923fe68a36263eed66bf392efc`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b91c3e8700c8b0c85ba0547c3942e90c0326cacd0d2f3902b7d57f2f20918456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f809398890e314c9318a6d9164f17b761b10ecfbb28e5d0cd5c891280b9a15e4`

```dockerfile
```

-	Layers:
	-	`sha256:0af5cc49310b1b8a2aeac190227a3ec0064d26834fe4b40e9022ae9b4816c66b`  
		Last Modified: Tue, 07 May 2024 22:52:11 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1621166ba0dc017b8428179fd95bd3b4fee5ca1ca789517cfdfcf687a4be0447`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:777a8bb0a527b4cbb6a46e10955382b10ab00d37d5e5398d1e968c45a9a43e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2411ad6d6f580148ecdc08c36cba909227e186cdc146798563d4ce0c23bb9e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581750bc7d79d641fc0050cc28574dc5206313581ff0ce1605dac31d2c6bd42d`  
		Last Modified: Tue, 07 May 2024 22:40:01 GMT  
		Size: 3.0 MB (2993744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d36eecf3d2dd5adda7641af7f61b307b70fe14c9c53a526cbaa49e011b057`  
		Last Modified: Tue, 07 May 2024 22:40:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:f32598d3e4c0f23b86cfa499571e93b63611c5367807c340e06cebc54ee37eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d75d0328aa1fea68e87949e476da8b155715a9fc7c4c2dd8f709cc73a67458`

```dockerfile
```

-	Layers:
	-	`sha256:6b744a5ecb4d41287d1199839b02e5ed8ecd84677fd4e707dad4bcd57ec7b73f`  
		Last Modified: Tue, 07 May 2024 22:40:01 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc81a3ecb005c2b9ae96a16c8ed2e799ccd3562e2bdb55b79607c204b669cdbe`  
		Last Modified: Tue, 07 May 2024 22:40:00 GMT  
		Size: 16.1 KB (16144 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:6a0f9727cba21820aa10182e21c212875e2e754191eca1e1058df039a3918b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d7f06fc750a87313184c7e216e40bc24ed18ec532c7da7f7447905159cabe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fedee3eb076f4edec0ad79368ec8fba8c732811f53420b731b260adca97e36`  
		Last Modified: Tue, 07 May 2024 21:52:16 GMT  
		Size: 2.8 MB (2834720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3dd0f8206eca60db7baa0cf436dcffcd2177c995fac02eeeea7471502879c2`  
		Last Modified: Tue, 07 May 2024 21:52:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:c2216f1ae9be40a1a25521d0acaf3552230a0bd1c535792aa31bdbfcd62e05e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47570ebb3fceaff881cc28e47caaaffcddc852bf59be4309b61694a48c9c2888`

```dockerfile
```

-	Layers:
	-	`sha256:967bce63ba883799dbfc5b9586dda2e57b4526814285efdf804cf0407af2db41`  
		Last Modified: Tue, 07 May 2024 21:52:16 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d57a338080e82e79357a3d257be6ae77ba70d2c0841701e70b102ec92c1f2eb5`  
		Last Modified: Tue, 07 May 2024 21:52:15 GMT  
		Size: 16.3 KB (16271 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:fb16468901234b2b45c13edb2d7a5ef3ab8bb497b2f5e10b21a4802e48a45fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6522680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a91e6fc105f7cfaf9089188016ea07df1e1d6754f451ef87fa3e6b945ac5f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd26f5b2cb8b657749020b7673d98786f88934f95e9b2f8f113132b35d2a1ea`  
		Last Modified: Tue, 07 May 2024 22:15:25 GMT  
		Size: 3.2 MB (3163987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec3bc802515906759e53fbfcbe2271c074504c170739a34a7f2244380714574`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ab50071d004a7b3d60b60043dfc324f1670e012824065484d63b4608078bf76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12741f55f45791ebba59d1931262666415d2eef5a9767c36745a21ff29438ed`

```dockerfile
```

-	Layers:
	-	`sha256:752440ac51778d8c12a8defefc3e348394bfa7c08ca3b6b40a9b6e39f787846c`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e20e6d6578ef3d883ec8e786ea027d261e454a25f680830566099acc8acbd60`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 16.2 KB (16172 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:94dd96e77bebcd5126f09b9bfe8a0bb1dbc06b064e159b69e013ca012747114d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6236912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a547bc0e3fc8d23c4ea9ee23f06660945f38aad0d1c471d10f5f5f757385dce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abbf3e89ee30c6e720fe7e1f847a18cc56ffbe94bb20bf653a1fa9bdbd71150`  
		Last Modified: Tue, 07 May 2024 22:56:36 GMT  
		Size: 3.0 MB (2993939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1504ce8c952fcccab833e07259d3bc7b8b7bcb143934bd1bd98702c6fb91ec`  
		Last Modified: Tue, 07 May 2024 22:56:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:714ff4ec0ad6ef85628f25dce228787eb85bd251468201646eaed89d630c3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 KB (124804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd31e225b0e25c2823f34f7b65cdaa37bec29b2b067b6d443dd3767d01d90cd`

```dockerfile
```

-	Layers:
	-	`sha256:850f4e1b6b59a6793c0c5445b4a541dbd263d8bba4e674d5f4678ce920af3edc`  
		Last Modified: Tue, 07 May 2024 22:56:36 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87c93ac9b7697ba13bc161e8680ee173b66092ef338725f561cb3b8f699df85`  
		Last Modified: Tue, 07 May 2024 22:56:36 GMT  
		Size: 16.3 KB (16300 bytes)  
		MIME: application/vnd.in-toto+json
