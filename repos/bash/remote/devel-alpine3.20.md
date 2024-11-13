## `bash:devel-alpine3.20`

```console
$ docker pull bash@sha256:2cc90a1639a114c99b7ac333cace515565666af465c05ac88fdce4722649974b
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
$ docker pull bash@sha256:a61024f8ccdbdd85bc073e35f1826b0e35eb0ba03ec138fddc467a7cf7cbb220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6537662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d2e821358b428e148174e6f0ac3cb7eb5515926b4aac657d7212f4a28a9d3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7326e9d8a08b865e7496ec05bdb43c4f8194172c0673787be49d09fc4eb8ceb`  
		Last Modified: Tue, 12 Nov 2024 20:07:55 GMT  
		Size: 2.9 MB (2913420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386729c130932ccba167e6948c80b21a5164bb92253102049d143d3c2e35650`  
		Last Modified: Tue, 12 Nov 2024 20:07:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:affae4ed9185e0a66a08329d5fee387c113dbe33d2c41b47a6baf16d7b111fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67ae9fd9786f1f5e2b329bee03c655057f92389c4f9c68bae879e81baa188d2`

```dockerfile
```

-	Layers:
	-	`sha256:a6217c4bb1262cc87579d731e575671dd651eba3835852546c78b3db10f1de28`  
		Last Modified: Tue, 12 Nov 2024 20:07:55 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f7a0afcec7aa44315ecfe9159dfc05df4ae170b6600b477aec7e18676623c`  
		Last Modified: Tue, 12 Nov 2024 20:07:54 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v6

```console
$ docker pull bash@sha256:aad7ce8072e4dd71e0f6639558cc4e3cc43785246b674df5a7a8604be6541660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1991d22a7bfcbe897a2193f65c31e58ef5b02f708b7cd7c3e63d2abafbb044c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd503485009a42692e0024eaf1adb93d23b1032a4b5e269b1cfc2eab0509d50e`  
		Last Modified: Tue, 12 Nov 2024 20:07:58 GMT  
		Size: 2.9 MB (2858623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca0ccbce9d954b2c85372b2096474a2bd1c812741054f8341d69814d8f9ad6c`  
		Last Modified: Tue, 12 Nov 2024 20:07:58 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:591c11f7fa2a8505304d646d6eb78e5c403c456de33c56ab5e4aa180b53bc157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 KB (16346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c8abf0673a0e27e98ffe51413662dbe2d8a8f7e9e616d7f928161364184e5`

```dockerfile
```

-	Layers:
	-	`sha256:ada4a3fa7abd906ea9db2c3f81a5c2bd631f2e8019ca46dbdd63ff4ee7cf4774`  
		Last Modified: Tue, 12 Nov 2024 20:07:58 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:c830b0eb920a4b22a89deee6d52bef19b78efb6c24fe0d39568a56f608ed9012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5898920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e34bb687f623c68b18c641364fe18a4b51cda897ba611452a0e62ed349689c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_COMMIT=0075715b29c9c1d984ec243cf3018775ed5612de
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_VERSION=devel-20241104
# Tue, 05 Nov 2024 05:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40b038656927938763f1d0d20810a9efd9f3083d4eb1c84ea2e571c28fbca35`  
		Last Modified: Tue, 12 Nov 2024 02:01:34 GMT  
		Size: 2.8 MB (2803096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bbf8bb96246a23bff41a316f521320fd7870b74d4e56cd7d5208986d4df1e52`  
		Last Modified: Tue, 12 Nov 2024 02:01:34 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:200c5a8c16fe0fc812626b38dab7164cbe0eb96ef1431fbd2bda75743da4d3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9f98157305511fb2d21b682a6110b602e63d1740b76ae90f76af83f1f165ad`

```dockerfile
```

-	Layers:
	-	`sha256:6cc850a777c95d47dfddeb78ed722fe99cfb3ca85d25743e2d65673346715fd6`  
		Last Modified: Tue, 12 Nov 2024 02:01:34 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4012f639d2c1e41995e417e92533043e372eeec4b638c002b77c6753fb8cabd2`  
		Last Modified: Tue, 12 Nov 2024 02:01:34 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:142b5829e2bd78ae97dfd5b2c8e2764db303f80e38a1f23fe60041cf6994784b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c1de8c2d18c442d09748de5c0aaf98f19b78fabb841eca26faeaa56ea403f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_COMMIT=0075715b29c9c1d984ec243cf3018775ed5612de
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_VERSION=devel-20241104
# Tue, 05 Nov 2024 05:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea97fd38eca3ae6b58e6c9ab8c77fa7b95823a88cc95aa1049b994aa329235b0`  
		Last Modified: Tue, 12 Nov 2024 02:05:08 GMT  
		Size: 3.0 MB (3008864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2169abdaaba59df00a7517dbbc55ea164797f1f8a22ed1c73c8949147795905a`  
		Last Modified: Tue, 12 Nov 2024 02:05:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:9f35706cd9e38119951d7975465c540def58a0ae7f6072ee23053e3e433b29eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c05d4e1567ef8349bafd78fc597593ab62788e63716fac57f4169172fd3791e`

```dockerfile
```

-	Layers:
	-	`sha256:04de082cbfe0d95fcb72650efb702188c3744bf0692a1b650eb9c392e074fe62`  
		Last Modified: Tue, 12 Nov 2024 02:05:07 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dea85d1783c50df06c45c1705faad692b1e3918ec41daff8413bbdc7ed0fce`  
		Last Modified: Tue, 12 Nov 2024 02:05:07 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:923c1bb9441a0b143abf3a09aee6807475918ebabcf74928749785f53df78afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6320028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967d935bf0ef577943035d46e11eee59297c89ab5747b92b8a95afb6748ac234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8c36fe225d26895c4ef80935220eff8085b3f3e774c9ea8bee5bfbc83262dd`  
		Last Modified: Tue, 12 Nov 2024 20:08:11 GMT  
		Size: 2.9 MB (2850470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91160895d8b465ea36e92944aa514503c1a5a78d370bb504806a0dcfba466583`  
		Last Modified: Tue, 12 Nov 2024 20:08:10 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:fcbddab34197106d2e21d51e54e272bffd85b7fb89bd70ff468b0e5064f85631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2074bed430d342934de15e84e0d94b23ecb79a18cb7247383782cb7a6720eff`

```dockerfile
```

-	Layers:
	-	`sha256:3959ff47f7f0f347b066f3e05f27de37c80d0d21d0aaa0ee402c7142bc412db9`  
		Last Modified: Tue, 12 Nov 2024 20:08:11 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e46fe038721059dbf70107ac63f1d41b122235aebbb71f369f73f24a05a7932`  
		Last Modified: Tue, 12 Nov 2024 20:08:10 GMT  
		Size: 16.5 KB (16453 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:6c0388e74f40d4eb7d79e267d1bc3f9e2836eb7c7ca59e9b2c9ab7ae35f764f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6753842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fd50684ce54b230c5d66877e79f81089a1ae311773298dfe91594490645e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_COMMIT=0075715b29c9c1d984ec243cf3018775ed5612de
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_VERSION=devel-20241104
# Tue, 05 Nov 2024 05:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c86225741b40b467173f962a84675fca0c0f1e365e6a93149c11f44e6226cd`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 3.2 MB (3181047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3700a80f0f6e761a2a94972d7b688990c15a03f1141b90ba7f8cb9d3a7dfe96`  
		Last Modified: Tue, 12 Nov 2024 02:01:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:463e92964400c7ebaffe11045ad0a709b3742501e36a3d4e2723d56c56240616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb49b97dab4ad17dbe0576322590e4e60bfd77b5fce6738a374fc215079a62d`

```dockerfile
```

-	Layers:
	-	`sha256:dfeda1e01055d20bdbb13f0e9f6739f4aaa7b1a1455cc6fec14cafd40b44ca6c`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5fa32fd43ca62d4f5ffaaefd35095603ad3c66efaf66c7c8c655487d6f82fe6`  
		Last Modified: Tue, 12 Nov 2024 02:01:51 GMT  
		Size: 16.5 KB (16454 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; riscv64

```console
$ docker pull bash@sha256:f10495431eed67c61baf9b76a3b5c1689b523abc90b9be8fbd914e80488cbbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e2dc069224793e529f0ac00aa4c45a5623bc097307d01a0e1ed4428bf4f69f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_COMMIT=0075715b29c9c1d984ec243cf3018775ed5612de
# Tue, 05 Nov 2024 05:18:33 GMT
ENV _BASH_VERSION=devel-20241104
# Tue, 05 Nov 2024 05:18:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Nov 2024 05:18:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Nov 2024 05:18:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2b641317a1ba6d943a2d7e1b6da1000103dde2ff86b713ff198984ce6418a0`  
		Last Modified: Tue, 12 Nov 2024 02:08:51 GMT  
		Size: 2.9 MB (2858318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c50f672966c59257162d934822ff3ff9aeb7d1ba321dfc84a4a973bb68af8`  
		Last Modified: Tue, 12 Nov 2024 02:08:50 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:c544e7a766d87eb5c31e7dc0d6b702d4210f349b17e3a3823a6a8eb1e6c004d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695ed58b32224d33e2dc5cbb513e6c3fc4f310589bcb2941adac0fe224483385`

```dockerfile
```

-	Layers:
	-	`sha256:c06dc966e693fdd4a22acd87c0aeb397673d0cc7f3cfe9f7ac3b36c5e8564981`  
		Last Modified: Tue, 12 Nov 2024 02:08:50 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c3b4919f568b7d324e5d6272e6645537f475164e4f39ce27998578a1a339a4`  
		Last Modified: Tue, 12 Nov 2024 02:08:50 GMT  
		Size: 16.5 KB (16453 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:9a1e81be31050bef77aee9eadeb858f27259da3bca77dd2f2d58a4d85442de37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b1d998443832fdfabd891116c6042c4496cc58a86cbf42c045c13acb3e7990`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7faa24e02ac27ac5dd6d1f44b6b81b88cd12fa9997e044a0c5ec69ac04ab1201`  
		Last Modified: Tue, 12 Nov 2024 22:34:39 GMT  
		Size: 3.0 MB (3009992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977bac542c835aadc0fdb7bbb58705b57fc8b9b751dbf456eecaba1b4135290f`  
		Last Modified: Tue, 12 Nov 2024 22:34:39 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:6d3c6ec15b27c00452d8375da406c12c4f253b50a95fcfa94e68e8d34e6df354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85a4174ce0ed6652f1cdca9820fe2e7e04ecf2c833ee827a8b1c56104efcfd4`

```dockerfile
```

-	Layers:
	-	`sha256:c324346f5f152db74a8eca7543ca31bc8955c5bc29622479032ce94b71200234`  
		Last Modified: Tue, 12 Nov 2024 22:34:39 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369568441e464bcc6bab6160963bd94338c1e2f495750b4bad15cf100da60378`  
		Last Modified: Tue, 12 Nov 2024 22:34:39 GMT  
		Size: 16.5 KB (16486 bytes)  
		MIME: application/vnd.in-toto+json
