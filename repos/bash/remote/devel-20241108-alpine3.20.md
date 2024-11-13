## `bash:devel-20241108-alpine3.20`

```console
$ docker pull bash@sha256:184ac60a6df09ccee5167f8de11095fb21b8c7bd9fbe58600cbb8a55ed9232c0
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

### `bash:devel-20241108-alpine3.20` - linux; amd64

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

### `bash:devel-20241108-alpine3.20` - unknown; unknown

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

### `bash:devel-20241108-alpine3.20` - linux; arm variant v6

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

### `bash:devel-20241108-alpine3.20` - unknown; unknown

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

### `bash:devel-20241108-alpine3.20` - linux; arm variant v7

```console
$ docker pull bash@sha256:1b0dd3c0a947963f95b167127657342bc8ffcc56364f1cf2a9f0f979bfbb031d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bed45e389cea4b4cb7fdadb6854e6ec37ef6dc4b862c9fae77dbf6713b642f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262b85e4f9df41f96d26cf4ecdaee037d8e3fb21dd4b7ee4183880cda7b9a8a9`  
		Last Modified: Wed, 13 Nov 2024 06:49:42 GMT  
		Size: 2.8 MB (2803323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11d3836e02ca895075d6f1bfae56fa2d3676fedd16f476fe88b421d57a81a5f`  
		Last Modified: Wed, 13 Nov 2024 06:49:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241108-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:bc9038980af263805be779b4d5e927f166e9d22b8672a624be6cdd2cc387f621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc8d7e08b1ee02c450c6fa79d7b4b9d780fc48136f446d29bde490dc33441f2`

```dockerfile
```

-	Layers:
	-	`sha256:747d7ef1c5d0bd9fde35821aafe607fbad5c44bdde3153888b9542ebf8ff9a34`  
		Last Modified: Wed, 13 Nov 2024 06:49:42 GMT  
		Size: 110.1 KB (110131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70eb2d57781fe43c1f06c66310dae1ff8ba2e3ce98d9701693a6043c6bf518a4`  
		Last Modified: Wed, 13 Nov 2024 06:49:42 GMT  
		Size: 16.6 KB (16562 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241108-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:c053d95149a0124a6b11586cdaa875f2dc6c50f7d4181a230eeeba934ec36176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7097232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e406f91c2f9393711dbcbfcf12f944d0bacf8b6149a7dee480213c477dec777`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f60ccabc38516a9654d03024092f7a507c06f37d3a6f11ed2eafd844812fdc6`  
		Last Modified: Wed, 13 Nov 2024 01:52:03 GMT  
		Size: 3.0 MB (3009176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6027497b212623d6903d7c0769817438f43cb985861b15e050c4c289d749c`  
		Last Modified: Wed, 13 Nov 2024 01:52:02 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241108-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:f0bf186eeca926e5e99a99f189bb352e5d0801562228b58cbc69375dc8648105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bff789f3dfaecc84c164cdeca09d156e491fc0ddb9cc2980b6d46d3e860f281`

```dockerfile
```

-	Layers:
	-	`sha256:4734c06fee94ecd63c6fb975fb015e335521c43c5f44fd8af1a6ad3003a62f6f`  
		Last Modified: Wed, 13 Nov 2024 01:52:02 GMT  
		Size: 110.2 KB (110151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b45a578c5e8b53239ce948b75c56aa42cfe6bd202db800f0d06921acf4907ef`  
		Last Modified: Wed, 13 Nov 2024 01:52:02 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241108-alpine3.20` - linux; 386

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

### `bash:devel-20241108-alpine3.20` - unknown; unknown

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

### `bash:devel-20241108-alpine3.20` - linux; ppc64le

```console
$ docker pull bash@sha256:acc37a392b563b2a4d5097d714db443feeb9c634da561899e5545bd37ad34540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6754190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e27c187d3d7acd4f7e7c65594a548b726418a1b1f43ea5b746371031a4514c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6169b0a3c632dafb87e185b377513bb732a83ae7302f6379abca37cb5d8e8`  
		Last Modified: Tue, 12 Nov 2024 23:56:28 GMT  
		Size: 3.2 MB (3181393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1828150e1e9e512404e405e62af6496db731c572647e4accdfabd031f6d70683`  
		Last Modified: Tue, 12 Nov 2024 23:56:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20241108-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:2ca8d21494ed671ab7b774651574926992b416d1b43d88ac432711bbc4ffc73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0224d10283104d810f0e182bcb5e92e1d95c59f30500ee0d8cd4bb6934154`

```dockerfile
```

-	Layers:
	-	`sha256:248338c89bfe1b2b0f49d9dd2a1823ae5d3feeb77155f932915f95e3c6af39e0`  
		Last Modified: Tue, 12 Nov 2024 23:56:28 GMT  
		Size: 108.2 KB (108175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62abd3d5d70522b403cabfe4361590ae3451d2c6927b007d18ba46cfbd637f43`  
		Last Modified: Tue, 12 Nov 2024 23:56:28 GMT  
		Size: 16.5 KB (16530 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20241108-alpine3.20` - linux; riscv64

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

### `bash:devel-20241108-alpine3.20` - unknown; unknown

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

### `bash:devel-20241108-alpine3.20` - linux; s390x

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

### `bash:devel-20241108-alpine3.20` - unknown; unknown

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
