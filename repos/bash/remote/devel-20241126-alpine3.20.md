## `bash:devel-20241126-alpine3.20`

```console
$ docker pull bash@sha256:53cea3c4a99ecba79fcb1a71f4bd6baafbbc934f33b91622ba1f5b322ab9eb39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20241126-alpine3.20` - linux; amd64

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

### `bash:devel-20241126-alpine3.20` - unknown; unknown

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

### `bash:devel-20241126-alpine3.20` - linux; arm variant v6

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

### `bash:devel-20241126-alpine3.20` - unknown; unknown

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

### `bash:devel-20241126-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:fa73385795c44cef6d728268889981be00321f6ec93dd2c6b90c6134fe1ef671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5908558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb057b2ee2dff2a14ffe98abae894c627adf6ba2eb9abd24850efb8140bfea9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992d28efd5fb5f287f1fbc6df3a2f3c9d5546000eedad2063bcd7247e53abb39`  
		Last Modified: Tue, 03 Dec 2024 21:26:35 GMT  
		Size: 2.8 MB (2812735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f595eaa86140af1c4d433814ec146b590d443882f97f94ca0553cc34ce1e12e`  
		Last Modified: Tue, 03 Dec 2024 21:26:34 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241126-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:e77cb1933685bc0107bd6df894f7e9ebd8b5814facbcfb4c6b92bbad78d29422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724b8ccda0e400fffda07a96d4362a63cd380f5d4a525218126e5d73d23d95bb`

```dockerfile
```

-	Layers:
	-	`sha256:56b18952ca41f7510c7f3963be062b23cb10d653707929c7b928542225511297`  
		Last Modified: Tue, 03 Dec 2024 21:26:35 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04fe1c474d3fff023ccf677279a7ae2e483a37e3a55ad8641fc92dda9dfb789`  
		Last Modified: Tue, 03 Dec 2024 21:26:35 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241126-alpine3.20` - linux; 386

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

### `bash:devel-20241126-alpine3.20` - unknown; unknown

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

### `bash:devel-20241126-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:f9f4eae32bf971c8e7ba0dc85b1198ca75fbd21334a726058cb90e0ecf927777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6763800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e6d778b60b47f2e13ea4c40133cb9267e643abc651ce8bbd94357bc9c4739b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8eacc04eecf36578c8c0fab2532742710b30d8f59404d3c7c21307e15a1cef`  
		Last Modified: Tue, 03 Dec 2024 23:32:54 GMT  
		Size: 3.2 MB (3191005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb28a844a38aaf16dcd19c2cb332a7487995b6402c8cc8dfe24fd02464fb35be`  
		Last Modified: Tue, 03 Dec 2024 23:32:54 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241126-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f1806d25b23b490111aeb2e95a702c66bbbc15dab4d8c6fb90f4a3ad61089634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee5ba6cab2685f4d1284101438bedcdca8b06eeaeaf5395ae5c6855a7c526f`

```dockerfile
```

-	Layers:
	-	`sha256:4b000325b568fc10e51aede1fd82e5d2cb845f5742a0ac37f788a1accf4478bc`  
		Last Modified: Tue, 03 Dec 2024 23:32:54 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251adfa2d9a5dfef506b07481794463b926e28392cc97bb2729ca56385855032`  
		Last Modified: Tue, 03 Dec 2024 23:32:54 GMT  
		Size: 16.4 KB (16406 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241126-alpine3.20` - linux; riscv64

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

### `bash:devel-20241126-alpine3.20` - unknown; unknown

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

### `bash:devel-20241126-alpine3.20` - linux; s390x

```console
$ docker pull bash@sha256:b4f8e8bf07c8dfc6529d4c3dca9e55b72a84fd32198797db62fa4b47d785d7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7630b865e1cb9b358101fb00d293234b6dabf97d97a7bb19c6858cc43a18f4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f1aa6d6b471439a242c5cd87859adb235bc160a27c47bf972e6559d9755b77`  
		Last Modified: Tue, 03 Dec 2024 22:38:29 GMT  
		Size: 3.0 MB (3019873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a335a3b5794a825e3b8b965c1dd54200568c3dbc209f90ea42caf9017ac208`  
		Last Modified: Tue, 03 Dec 2024 22:38:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241126-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:1c419b1152a9ef41df34ab61479df6f0420c369d9c4997970e6ef822d69d8704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cf776d25a3b6258f5b1251a0d62de1a1cb232e5ce97b5077b1259ac2261210`

```dockerfile
```

-	Layers:
	-	`sha256:52105e50cde5ef2dbe3a2757bca79f7d09542d689b9767bccdcac5fdcadd03a4`  
		Last Modified: Tue, 03 Dec 2024 22:38:28 GMT  
		Size: 108.1 KB (108141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503b7b2a00901068b174954c0a5d5de94937d0b685237591c53799c59dd576d7`  
		Last Modified: Tue, 03 Dec 2024 22:38:28 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json
