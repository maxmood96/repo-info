## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:d338c86d06fccbd348e402d1e4895786b2b65ae1a8d55322a6a1dd2b339ded14
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
$ docker pull bash@sha256:2dd5afebc54a1cb7fc2e38edb549c87e0dfa2b48afe69b38a9abf057ceac8782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6544685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977a8a15bc9e7c1f0172141ae058a11c2083040a478edba05ad63a7a80e2d9d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9919b5f418e976199f0b7775202d96c04e7d552fab89aeeda21e84f77f3eef`  
		Last Modified: Tue, 19 Nov 2024 20:25:00 GMT  
		Size: 2.9 MB (2920448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e2075f4b052bd39bec14b4eab1eb9140824e9014a2691bb19061158985b626`  
		Last Modified: Tue, 19 Nov 2024 20:24:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f0691e3fcd48dab66ace9ed95add22789efe595d25d8a14a38dd26ea2e3279b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5e2b25c0685766d12f5cba3c90413f4d8f133c7b08cf65c748e77810e5d9b7`

```dockerfile
```

-	Layers:
	-	`sha256:276ea161966c7dad6174f034bd96395bb9aaf4b198c45cc9bb4e863f46e100e9`  
		Last Modified: Tue, 19 Nov 2024 20:24:59 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bdcf116a206bbf21b11887e9cb7febf584b038e9406f5974903106d6476c22`  
		Last Modified: Tue, 19 Nov 2024 20:25:00 GMT  
		Size: 16.3 KB (16270 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:48e4129566ffbc26e46e451d851a10b4f0a9c8aa7fa44b3e0fa3f2f1c60ad7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6233296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3569004ca005ef879a1cc44f06a7c153f8c3b7cb037ff465a11edcabe511734`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365c946e5fc6ff9d259fcef5753eb4242665fd198179f4952d9860b8d05ec2`  
		Last Modified: Tue, 19 Nov 2024 20:26:45 GMT  
		Size: 2.9 MB (2866361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf800ccb327e33b93aa0ce8a3caf1f89525376c1ad7b115c802b094b0ed0ab7`  
		Last Modified: Tue, 19 Nov 2024 20:26:44 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:d8e5595473f4928d441c814b89f010b6119c7419360a183833aaddb042fe56d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca33b29284966518a4446ba659ee2fffd5baa71b6c58efce1e66cd1c2d08b6`

```dockerfile
```

-	Layers:
	-	`sha256:8d056e108ba0a35d7e13912821a6b29a9eaaf2ebd510547fcb401d006832a5da`  
		Last Modified: Tue, 19 Nov 2024 20:26:44 GMT  
		Size: 16.1 KB (16130 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:80b9cc99e074918770233296405a38179b18f8fa9037e7f5ef6d714f4e2bbc19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5906726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4476669d66a088ba749353e4f1108051d024718a8558ab9d2925e5e00a36e47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0e0d9e33b6887b8e0586fc7903330588b5007419fc6c8629e3b75d6c359487`  
		Last Modified: Tue, 19 Nov 2024 20:24:47 GMT  
		Size: 2.8 MB (2810903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26c1354447d797466607db24442b8c24cf05c4b3ff72b1bdbc1a1e903b5d8cf`  
		Last Modified: Tue, 19 Nov 2024 20:24:42 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8ec95b4cbebeb47fb69d3cf2df71d9d2583c841a27b562c8ec9bbb7957d673ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc940ad41e8b3c43824d4bfe80ca229fee1f9b006e76d22b56365211f6c112f`

```dockerfile
```

-	Layers:
	-	`sha256:502b84d667cef3ce6ae2408d4fa5f721754c66ad34d6adb1cf0434c566ebd65d`  
		Last Modified: Tue, 19 Nov 2024 20:24:42 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:201f69a8e2c8db7f3450d5fedf2f08b517202803a78d1b66d8a091a30a8e3c34`  
		Last Modified: Tue, 19 Nov 2024 20:24:42 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:c6ed6c183d1bcada0bd05aa7ecea250c55b46b33de93a5ffb43cc028bd2dde03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7104583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c894add3d337c9368261bef9f53aa6c058a3a5147d89e748d5d437aedc4ae293`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4847362f1a62096228d93fa7a7af98109af02491671a893c095a6c9e0f8782`  
		Last Modified: Tue, 19 Nov 2024 20:31:30 GMT  
		Size: 3.0 MB (3016519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0ed545ab0c315a89f136510a38d0f482066a8274a7a97512f0b8f9cc27e230`  
		Last Modified: Tue, 19 Nov 2024 20:31:29 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8adbafec36d48de0fc27c29cd597bafa0feaf6397c7c1f78381592d005c7543b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddfd4f94b16c4f47b49241755e8ec328afa2589063c37ec74fa0ac79e17454c`

```dockerfile
```

-	Layers:
	-	`sha256:727d1e25841a9d4954d54c9f44ce6ffcf6eec61fc56961df2c970dc0718f183d`  
		Last Modified: Tue, 19 Nov 2024 20:31:30 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfee5c40c1a49354f158e8a64c4c2ec8556ee8d6da4301bf563d2956acb8fc0e`  
		Last Modified: Tue, 19 Nov 2024 20:31:30 GMT  
		Size: 16.4 KB (16374 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:f5ddd958e5db20bb5ec26e0f40781c463f849815b98f7f748caaa8b31a7178b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6327665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e945df8a513f5b457f82f37294531e0733d2f64e15f123e616b6f5f7ed86168`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236f1f22c972cd66785fd5d0777c431d325cc6ccc4787aa2fb8d6e6bfe36128`  
		Last Modified: Tue, 19 Nov 2024 20:25:08 GMT  
		Size: 2.9 MB (2858112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99d13c4d84fbef2e9e1871e4532bed49d5c52b55b59c0630f4ecb6ebf9e95c6`  
		Last Modified: Tue, 19 Nov 2024 20:25:07 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8c5a9deadf39a4941541dbe45919cb15d2dae686c7fc348f28bffcc14809bd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 KB (126308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0b386b2414c9b165e23439a23a48ac08f6f3dc7615818c0c2b64ecc584ccbe`

```dockerfile
```

-	Layers:
	-	`sha256:e0b3ad308a44a974f38bd5354c9996fad1c80e1c4c4d7028365c2ca40afd3d6b`  
		Last Modified: Tue, 19 Nov 2024 20:25:08 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b376a463650b62ad5897b7226ecfc3332ae5e92a46893bd495ccfbf1bb480b`  
		Last Modified: Tue, 19 Nov 2024 20:25:07 GMT  
		Size: 16.2 KB (16238 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:7c5a1e7b5a390a7ee5c6aa81f6e15de152b98d1d57d2838560b5ed941735bba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6761288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e109876266e00ab65fe7fb5d53d6f02625a439403b619e3099509516075b3c11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa0d8a577633681622e26a79a748f2ac40d2235be5660384258b918d4b04f88`  
		Last Modified: Tue, 19 Nov 2024 20:26:46 GMT  
		Size: 3.2 MB (3188491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e59cdb1255dba43ee5dd577e30430cb61eb50a777e6c432c2f82ea337680baf`  
		Last Modified: Tue, 19 Nov 2024 20:26:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:8d2676710d612cb0d2c4e335fce840b77aa599701146b896c686b1b756926226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee04220354f6815b78cf4a5ac98632d61d475e70c64574f375678a1e0066cee0`

```dockerfile
```

-	Layers:
	-	`sha256:858a60ff89805d73f1b9d0c4d6656d088ad29b0e151694ba572efe82e28f7774`  
		Last Modified: Tue, 19 Nov 2024 20:26:46 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf751feb9062c0a65bc4cbdc7de022297c89454adc47cf405879cc7d361424c`  
		Last Modified: Tue, 19 Nov 2024 20:26:46 GMT  
		Size: 16.3 KB (16313 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:36ad1b414869854f1c71a6dd68943e468776558249d856c8109609213c281f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea36a88247f9f09b868e7ba6693c3c15c2f079166fd21bd09171189ff2bad488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 12 Nov 2024 05:18:29 GMT
ENV _BASH_COMMIT=b116cfe57df2c061cd953b77a0fc1b738dd5fe94
# Tue, 12 Nov 2024 05:18:29 GMT
ENV _BASH_VERSION=devel-20241108
# Tue, 12 Nov 2024 05:18:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Nov 2024 05:18:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Nov 2024 05:18:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Nov 2024 05:18:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1007f110ddb21e54501edf64e328bceee05d0945c9cecd8f763eab35680bc98`  
		Last Modified: Wed, 13 Nov 2024 11:48:55 GMT  
		Size: 2.9 MB (2858705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75327cbf11e785a913752f82d6e8c9561a1c71054444b05c47139b88bb1567b8`  
		Last Modified: Wed, 13 Nov 2024 11:48:55 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:1206d07072928325cef1448b56a80ad2973eb295f3b04ee15da0fb7badde2e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70ece810d700b66064684fc1b82c917e72a4987ed470e30c0f7f8dacd1706a7`

```dockerfile
```

-	Layers:
	-	`sha256:4b6ed4ab736860731e278ac347364eaf6252e38461bba00fbda1e6b8516c5e08`  
		Last Modified: Wed, 13 Nov 2024 11:48:55 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d56e1c1650a07b931dfef61efe00f844cda406cc2455093e79e66f60a44f0628`  
		Last Modified: Wed, 13 Nov 2024 11:48:55 GMT  
		Size: 16.5 KB (16530 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:0033b476b526984e7b00f367e154b0b03bb63adf2ee80a03d3b8c45199006099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b8d864644bbbf2325c501314b0329b2b1854c2ad8362b8fe5b5f5b9dafd74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_COMMIT=fa68e6da80970c302948674369d278164a33ed39
# Tue, 19 Nov 2024 05:18:25 GMT
ENV _BASH_VERSION=devel-20241115
# Tue, 19 Nov 2024 05:18:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Nov 2024 05:18:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Nov 2024 05:18:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ecc9cdbbcdf8d1d6a8567c39bebb03a30dce5f13695cf6f03a128801f54280`  
		Last Modified: Tue, 19 Nov 2024 20:28:34 GMT  
		Size: 3.0 MB (3017429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b466c005e690f019a0e0b8b50b087465ea63eac31e10d3855a04cf3dd1d7ed95`  
		Last Modified: Tue, 19 Nov 2024 20:28:33 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:b8b2f8ed186dcd68ca354d87bef73a3279bb73dbb8d1c2524a3c8cfdc10d5c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 KB (124411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c64cecbba2bbda4c7e8dd817d17875d96420d8312e198725233be25f9da90a6`

```dockerfile
```

-	Layers:
	-	`sha256:0cc56280e8c3a98157796a547a6969c9403af3846ccdfcb63e8816acc97da8f5`  
		Last Modified: Tue, 19 Nov 2024 20:28:33 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e21c90fb15f86e804ed0098b48d92927a7e20f9f1a092fa887fc29cc7d3bd7c`  
		Last Modified: Tue, 19 Nov 2024 20:28:33 GMT  
		Size: 16.3 KB (16270 bytes)  
		MIME: application/vnd.in-toto+json
