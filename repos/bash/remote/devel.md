## `bash:devel`

```console
$ docker pull bash@sha256:c9d2e27d3fe21f90594e42484d1453747438903926485c19b29e55b1a80891c7
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
$ docker pull bash@sha256:ff370005aa7181075c6ef8270745446c40f4cb28439a5fd354b1ee0f1f9984ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6546365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d917279812926456d5ee14adcb6794ce5a51a9c4e8b40ae8008d1b2ed8f01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_VERSION=devel-20241126
# Tue, 03 Dec 2024 05:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3ff726e5a80049b1567658d8843d8c9244aad253f73284ecc2330b2c4735e6`  
		Last Modified: Tue, 03 Dec 2024 20:29:12 GMT  
		Size: 2.9 MB (2922128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e5609ecd601087feb5c045d856418c85ca0e45974f88a3f257f5fca9a00a8a`  
		Last Modified: Tue, 03 Dec 2024 20:29:11 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e4e6c747e4656355abf8816067520912f26555c0b84470cbd2df3193e4693aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47253aa34c5f7efd1921d8607fdedf24cbf25defd71a7d6867eebdfd19d006a3`

```dockerfile
```

-	Layers:
	-	`sha256:fb8f244e61a51479f69c3c9739566fc35a46e673b5d218b27568b9ca1a53b85e`  
		Last Modified: Tue, 03 Dec 2024 20:29:11 GMT  
		Size: 110.1 KB (110095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c807d83e65b24011d4498c5b416ccd8946a25d6bd6ca3a7dacfc1e1edc0000b5`  
		Last Modified: Tue, 03 Dec 2024 20:29:11 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:d18f9184d7fe25b0e34b2bee68087408556516cf00906e597e722661942a46a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce740a1bdabf5bdf942af5a481f1e7014c78de999c4c0febbdaf3b97010b5f2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_VERSION=devel-20241126
# Tue, 03 Dec 2024 05:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90441a48fbb802a3223b9646d0512034e720b7fb7101a92cefd157b8ef4bd221`  
		Last Modified: Tue, 03 Dec 2024 20:28:37 GMT  
		Size: 2.9 MB (2867735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748cb92a2835de2fd86a64054859010278762830a5907c515b94e100e2efb911`  
		Last Modified: Tue, 03 Dec 2024 20:28:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:787039dc4dd1b18314681a93043e46f719610803757071daccd6d395ca2caa97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cad5030a460b9b2bd10a7c27a13f5cbdaf0a7ff93869c01412d48edced5338`

```dockerfile
```

-	Layers:
	-	`sha256:e4c1e79b1efd7d3153966e9b304f4d06bd56d3e97a57e000ff34a992faf1ec46`  
		Last Modified: Tue, 03 Dec 2024 20:28:36 GMT  
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
$ docker pull bash@sha256:d26dc52d5deba537dc48b2c80edd5bc24d60b391976b7fd2707ad4a075298789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6330700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa1d25102a6f8e2cf20e6c93a99a1a77c8501c8009b5ec4e012b10fc65ba54e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_VERSION=devel-20241126
# Tue, 03 Dec 2024 05:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988409c8acc69fb7410af320827b43754b1dea60d87a88ba99c3c07d56f683a7`  
		Last Modified: Tue, 03 Dec 2024 20:29:16 GMT  
		Size: 2.9 MB (2861148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea0d60d7e907c8b500dd242eaa493e540b0ae5d7ff6c91a055c537af2bcbb2`  
		Last Modified: Tue, 03 Dec 2024 20:29:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a19f78ebf45aa869ec1a3ff71d16a6b98186d02b58aba64a47104f16d14fd718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8329b9250c37ef1054a4beb2681d992d066585dcbb87c2673630c71dbfcfbff7`

```dockerfile
```

-	Layers:
	-	`sha256:d63178b9a30e22cc4fc8cadfc8776add002ecb5960b8b7786078987d7a9f5625`  
		Last Modified: Tue, 03 Dec 2024 20:29:15 GMT  
		Size: 110.1 KB (110070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8fd9e565bcd65313e5c8600c8c7faede72a610878c41ffb713c59ac4c37eab`  
		Last Modified: Tue, 03 Dec 2024 20:29:15 GMT  
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
$ docker pull bash@sha256:916a922006b94f24572edb3aad8b2684e35b4ee5490a8a9a2334aff79c0baa81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6238752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d96fc777ac9f53a8d015d53543f116d47750ee6c7b45e611df8b9bbcf8898d02`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_COMMIT=49c2670226b045746d66765b23af37c1c7ba5597
# Tue, 03 Dec 2024 05:17:57 GMT
ENV _BASH_VERSION=devel-20241126
# Tue, 03 Dec 2024 05:17:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Dec 2024 05:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2024 05:17:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310aac4cafc7c95b52bc14a776561424688f45262b86ce1e6b69ccb111407c70`  
		Last Modified: Tue, 03 Dec 2024 20:35:39 GMT  
		Size: 2.9 MB (2866928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0facf7b5d582f2a20476194d6fe5aac2d3d20688ee3462df94ceba45775707bf`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f36f467571d4b98aa5a20df282be91a56bc1580b71e372eae976bd83ebd05aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdf3ba7235f7345c825ae662956f0abf55b769d83931b6b88a9db425f9319b8`

```dockerfile
```

-	Layers:
	-	`sha256:6a3be803f83a9954734b7b6eb2035f1af2fd914b013b8c9dbd045dc4c069acde`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
		Size: 108.2 KB (108171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d3dbe9383277b2208bf28e42c8888f47b7867588a30046c8ff3aab12f9b795`  
		Last Modified: Tue, 03 Dec 2024 20:35:38 GMT  
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
