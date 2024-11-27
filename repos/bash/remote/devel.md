## `bash:devel`

```console
$ docker pull bash@sha256:e963686f14bd7b7154a0ec590a2b75883783248e3fefb078b8cc0d8bec769f67
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
$ docker pull bash@sha256:133c39b6e894cea4514623864891236dbba63511eae2b8d55ca494ac730e8ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6545764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a320ea0c682ef8f8b9a14b0a7ffd08101421fbed35053b748d0311d93e6200e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c23c680844a28f532869b6840b0af92287e23604342877af6c2f110df841af`  
		Last Modified: Tue, 26 Nov 2024 19:24:58 GMT  
		Size: 2.9 MB (2921523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7f2113cf1caa9002ee01ae75aec717f9396c05c3e9cdaf3a71d784e4d1d1af`  
		Last Modified: Tue, 26 Nov 2024 19:24:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:70f93895928e05957fa0950f99cb25d54f5f08b65e66c6a09eb5de1452a70c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9023b6c301c30e9dd5e5105506924bcf13f4004c6c052a60e180e44d1d7eada2`

```dockerfile
```

-	Layers:
	-	`sha256:1da81c1f5818c60e7a338a7fee713c612223d6fcaa4bea2e00f066ca4b301327`  
		Last Modified: Tue, 26 Nov 2024 19:24:57 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1982759f6d0a6b02d958c1e465c66d0c2e5fdd867c0b22ca85d2c4b209da419`  
		Last Modified: Tue, 26 Nov 2024 19:24:57 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:e5e6cdcf87b6411a0e6d0cb3cc33a5f3eda8e9b734af446e345e60e9fe00621f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b4e56c5d57a282c5fb31e03c09d5ee2f08b7bfd43202e2ef37c273f3997487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80278d3b89cd70f10bc17836210d9d99def1d94c83630d1f872bf34b0a7e5b5e`  
		Last Modified: Tue, 26 Nov 2024 19:24:55 GMT  
		Size: 2.9 MB (2867561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84077a7fb7b19be10059a485f1c68f385b7c3966c7bc047f2dde12a0acacb341`  
		Last Modified: Tue, 26 Nov 2024 19:24:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:31e7450be21928781ae1f168375a720380078ebac2a092db930c9e88de7e4ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af8f87c6ddb4a47bd719ea565cf80311b4df0c454bd0c35459b3b31d568231b`

```dockerfile
```

-	Layers:
	-	`sha256:fdee31c64835ab9a67d6767f72366bfab21fb99526c20e92b63a106d10088014`  
		Last Modified: Tue, 26 Nov 2024 19:24:55 GMT  
		Size: 16.2 KB (16223 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:89f8ece141e77cc5dfffccd4032fda16d190dc9f8c67eb6a6a1efa87ba9e0727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b0e746cd7e29d127c464f718583fc4eea2ad2f60c16e2cebe41a3ed5cd4441`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5436596aee55d3531ec0a826267d34992f5007cc010a039e3734a910d543acd`  
		Last Modified: Tue, 26 Nov 2024 19:24:37 GMT  
		Size: 2.8 MB (2812204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3904f9bf76620556e37c9e90564aa11279d4dcb71f56fe390fa4c1c319a2fa93`  
		Last Modified: Tue, 26 Nov 2024 19:24:37 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:4568e4d959332a3f99204c0c0ed7f9092c271e0d1d29b8d51bca86c6e402da59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5962124e523bd5ece7178aa04daddaa1740835c8c7d685e488553f7c4e24d3a5`

```dockerfile
```

-	Layers:
	-	`sha256:8f4eed1ef3e0e831c5e96d2bb96aa93e125a45a256a3f296dccf58b1a38d9238`  
		Last Modified: Tue, 26 Nov 2024 19:24:37 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:951dc07b6774de63ef320fe801d8e55708e4121756bb908e9f602ae27fd55d1e`  
		Last Modified: Tue, 26 Nov 2024 19:24:37 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:a4f977c180c82280950149f59b17d53ad80b0f852947bfd3559264be07d04b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7105993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d923c3a9d330350f4dc35473954c2441b0abf91526aa4d4847fb4d5b1044eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76243f1894a91ee443e25e88a8af2d53dcd872b362075017dcad86a23b778f3e`  
		Last Modified: Tue, 26 Nov 2024 19:24:49 GMT  
		Size: 3.0 MB (3017938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3092a539b45c8b69b23211c255e53844e1f15a696207e0da6f66b27c1fbb83`  
		Last Modified: Tue, 26 Nov 2024 19:24:49 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c1ce08bb050f21a937719e43c54642877243d04e0c37a7fc0a5be8c02f7a93ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7db7c7a111ed4e5f5a3b20ab3cccff32d5621bd7170b680467ad9ac548de7e5`

```dockerfile
```

-	Layers:
	-	`sha256:0dab31a23e59cb6a0d775ed84fd6f757832d8001cd108d97867c76e11543d488`  
		Last Modified: Tue, 26 Nov 2024 19:24:49 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336313d3fc21a6f33cca3b190360db545ef568f2875a509c7ecae3a93288312a`  
		Last Modified: Tue, 26 Nov 2024 19:24:49 GMT  
		Size: 16.5 KB (16466 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:68c59cb5a79217afeb334eee45bc5c5469b6e4f575fd68f91df020fa74cf597d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6329782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558f71347cb50bf0fd9d23fb780bf8679331126baaed4d5b15f9c84b0f71ae10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3d42ca8c4d54b0734ce5273e4821395f49d97038fc5bc54334a399243e6400`  
		Last Modified: Tue, 26 Nov 2024 19:25:00 GMT  
		Size: 2.9 MB (2860226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f846e4be04ce8f4f0b08f10e76816a61028de8ce59eb901c090cba8abb3ffd5`  
		Last Modified: Tue, 26 Nov 2024 19:25:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ed2abed91779f6332ba3b087b56852f33b00be5b696f6fedfa5437e67e9a6419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03030ff5e5ec140457db8236a2442cb3f8334f4790fc0458a61e1c9b820c11c8`

```dockerfile
```

-	Layers:
	-	`sha256:d8327cc34cebd2c50a8db70a28fb1b17ac30e59a8f0297a737fdc24d3fbf96d1`  
		Last Modified: Tue, 26 Nov 2024 19:25:00 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e20a6b65a2321f1eced2fd0e91f152d6753010368a3e176a52c55a12fb0119`  
		Last Modified: Tue, 26 Nov 2024 19:25:00 GMT  
		Size: 16.3 KB (16330 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:8c9b0dc2743c9681c80d62e890a0790fd20cbf6faa7b8cc20878e2b2af92fdb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6762833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192439b2415ae6b4e0b5e88ae906ff0c9e9da7aa710299713ef24a2ce88e5a79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e438d15ea163beb4da4994a16afb44788d65c3ea539affaf89cad18f42721dc0`  
		Last Modified: Tue, 26 Nov 2024 19:24:57 GMT  
		Size: 3.2 MB (3190037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c672c88cbb525ac8f7f5491d30ab083f57eeeb4aa73680e25b173b31ca916d54`  
		Last Modified: Tue, 26 Nov 2024 19:24:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0959dba744eedf095e51adceccc8dbdd37d45df6892fbcbdb61780072a0a4067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86418e25ae4b98c4e84432286f780806aaf27a7ef48be39c1abdebe3eac8b973`

```dockerfile
```

-	Layers:
	-	`sha256:ee9576d09f283034647acac7b70835fbed05265277527c343cc5151451314d8b`  
		Last Modified: Tue, 26 Nov 2024 19:24:56 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62416fe5e218f135193dc60dbbe335b1d4a3ef5a99caa3e178fa88f01dfe634`  
		Last Modified: Tue, 26 Nov 2024 19:24:56 GMT  
		Size: 16.4 KB (16406 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:9c20dc6b7b054be0df3effcae02e51bcdef217edd194de49867e95c28ec57fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6237927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f2fbb6d8e967201167b88f499202557dcce9c11bccd777263841edc988097`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554d9eab5197b499116d8ba5f2ab3fef8762b7ee5ae4dc950a09b096d8b0ab05`  
		Last Modified: Tue, 26 Nov 2024 19:31:09 GMT  
		Size: 2.9 MB (2866109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4876782dec6c7d99582c8bd920dcbce8d7794b1afe884f31e20a4f346b9906f6`  
		Last Modified: Tue, 26 Nov 2024 19:31:09 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:87d5b83c40303be7a8d487ec91169e77d65c83ffc97b192cbbb2f0d3fd0d20bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c6f25e22dd40e17eab9379e3e1753b3ab7acea6bbf7728cc18148a5f37aafc`

```dockerfile
```

-	Layers:
	-	`sha256:389e39a6b661e1376d44a3f30215f6b483c6c663375689ab5baed2c94319d733`  
		Last Modified: Tue, 26 Nov 2024 19:31:09 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7e916a663d3df608643784f180431ee542adf8bf59b8c25906a878eec5c4a2`  
		Last Modified: Tue, 26 Nov 2024 19:31:09 GMT  
		Size: 16.4 KB (16406 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:4c785b5e0b7c3b8de6d3c563082cd9e728ab31e3d92a64611afd2850b0e119c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441acb3fbe985f79badb4b600561286ab5f7fc737b67afe0a655909b34ce224c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_COMMIT=22417e78816237ae66f2da661567dfe5ed3452a1
# Tue, 26 Nov 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20241121
# Tue, 26 Nov 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Nov 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Nov 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904d3abf798091a9cf05bdff112eb29809763dbc06237a8bd6884daefba63ad0`  
		Last Modified: Tue, 26 Nov 2024 19:25:42 GMT  
		Size: 3.0 MB (3019514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c815f1ad9be88dd61dc4c7b8d041babfe4e7c9fba9e0ffe9ebecbe62a26436`  
		Last Modified: Tue, 26 Nov 2024 19:25:42 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:23dd535ffd399209bd72e3652a5e5ffcc3f299cd005d2e6a81a8e80ebcd86a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f40c02883927f4348aeed8f0015e3024f67dd9dde4d826c2452c2ace466fe9`

```dockerfile
```

-	Layers:
	-	`sha256:f59b02d2363b947211b770a0b424eb61095f626967543bd598ebc9a45acab5d8`  
		Last Modified: Tue, 26 Nov 2024 19:25:42 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda172d5c741d14dc257a6624f863a3c9a9e89ab1968a44172fb7f3cebd17af2`  
		Last Modified: Tue, 26 Nov 2024 19:25:42 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
