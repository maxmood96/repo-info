## `bash:devel`

```console
$ docker pull bash@sha256:2781166f388dc614a119d7b192d452fbecfe7f383945088b69aa48fafe2f5741
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
$ docker pull bash@sha256:b47c23aa81e94cca4c8082b796977de5f5681602e7848c8c7fad1ec7db8aa18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6531543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97546bc70ceebce65f81ab013993b55682b3df8980cde9990996fea884efddd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2a2831c60d84b8e016a252217cb80d523362dbdcccbc2b5beb53e129068689`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 2.9 MB (2907398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec69aaf8ed0380481ddda3ebd9cda123aeb5039bac62439d8564ae547c8632d`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1f8f427ae4970ceab77efcd9d7377fed81d05b84e9cc56689ac2b86150d3ed6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a1b7c14889d1154b9fe6053b48ec4d4cae34ef56b02ec523a3fc22eb9ea45b`

```dockerfile
```

-	Layers:
	-	`sha256:42a247538cedee4f4357e238113f22fdc056e94c56b9fa80a0718ac86465254d`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 109.9 KB (109896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c001ab3d687fff09076448c3226d7c2c568978e319ce748657e347af357cf5ca`  
		Last Modified: Tue, 01 Oct 2024 22:19:27 GMT  
		Size: 16.3 KB (16291 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:f6f6c81051f17d757aefbed24d6b187f67e8f60b52907a8433f76d11d8e28471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f17268b1232e3cfb6e3c27d806f00fa35a754cd225b66ad249fd90ed5db3010`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c78987ed60826446aa2e753fc9924fb5a9f4eabeaf5ed511bf10563f8c136`  
		Last Modified: Wed, 16 Oct 2024 00:57:21 GMT  
		Size: 2.9 MB (2857326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4412e2742a43b98b2e14a737dd4fe5a7a017737a271fb388fdf7484c89397edc`  
		Last Modified: Wed, 16 Oct 2024 00:57:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:810e2be9de54e8f65349465361207a7d4c3e8626719e730f82da04a29a59ab7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d6dbf12d3641d8a35433f23fdd8ad1abffc4109b30791a3cf71d8b44e8d7b8`

```dockerfile
```

-	Layers:
	-	`sha256:2ff6682e2aeee8fe01e9e53ab4779bd857d805147b0aa8de1148c1993e62590e`  
		Last Modified: Wed, 16 Oct 2024 00:57:21 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:50e01be24592fc37983570ac5e4dfb369df7630cc03a6c63ce7b1a46d70c244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5896285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc57a2b81311d0d0078ab7b0b80fe02d0206ee5a6ea990c94ddaa1c34dad316`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eee476e44975f1e86cad88b3023e8489c85524e2391f06b992c36780e8f802e`  
		Last Modified: Wed, 16 Oct 2024 00:57:22 GMT  
		Size: 2.8 MB (2800453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbef29fc00825ce0cf68c7fd1f1b03a58ee24a82b228b05fd845cd0e616892e`  
		Last Modified: Wed, 16 Oct 2024 00:57:22 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d3029de1603fd033ef0367e1b9de795f26e7146281f637a7952bb025e1fb43e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d85dff30a59169bb66fd44b45443dcfea9d9e4001626e1410d3ba46f0404bdc`

```dockerfile
```

-	Layers:
	-	`sha256:0acb3cee579e6a0e177a73584cfdc5584c1403908312474d6885ced29fc4ced3`  
		Last Modified: Wed, 16 Oct 2024 00:57:22 GMT  
		Size: 109.9 KB (109932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7e9b2ac9e21d76338646875ef8b74f534530ecd023465270ad87a269b1be71`  
		Last Modified: Wed, 16 Oct 2024 00:57:22 GMT  
		Size: 16.1 KB (16146 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:2df35b12fb5812c709d663a769d7dfccad50b53aca995c65a31490ac5301056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00688a51561f1d71d052ad86f5910dfc17c58f36508a4dd66c1145d8eaaa4406`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0deb796b5d50b9b9a913f9c9cc6b324a477d7ffc89955f85bb1677d43b8c48`  
		Last Modified: Wed, 16 Oct 2024 00:57:18 GMT  
		Size: 3.0 MB (3006699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c714787b15a80a2715da9897d69d07febd91ee7c9c997ca60fabf71769e973`  
		Last Modified: Wed, 16 Oct 2024 00:57:18 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3f985d69e85560ea0cd245dc253698797fbcd728eb6a2e211f1bef5f0e3c5242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607dbd0d6632d218edb84ba241cfcf78f75f2f2a869b5e710af6654b05707771`

```dockerfile
```

-	Layers:
	-	`sha256:6301befeb38904a741037a33c21374ba85f7a5c76f383fea751772a45832b73a`  
		Last Modified: Wed, 16 Oct 2024 00:57:18 GMT  
		Size: 110.0 KB (109952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a9007ecf6f4e6bca7a45222a583870374691318f8c3fbcd03d2702aa64ab2d`  
		Last Modified: Wed, 16 Oct 2024 00:57:18 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:edc19c5e22db576d6d2165625771acb72ea7d9607b4cad6125dbb17f8675aefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6318494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e186b914c588fd4bc23655f5554e1ea8143490d4fe25897d654791a68c93f9d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_COMMIT=254081c09767738833cdf161b4bc3feb1a51690a
# Tue, 01 Oct 2024 16:40:17 GMT
ENV _BASH_VERSION=devel-20240927
# Tue, 01 Oct 2024 16:40:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 16:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 16:40:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da69b259ad33078e78251f1aa92d613a943877af9d05b80a363e249d28ffb771`  
		Last Modified: Tue, 01 Oct 2024 22:19:22 GMT  
		Size: 2.8 MB (2848997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301c87eee57fa04e3388297ed1861ed796d0bad007b294660b3e45a6ccd8a210`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:20c1aea92d1bc72fbcea1bd04f470c0340845bdfd1d7fc0acce264b13d987002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a780a92374fc43358b326de740bfbcfd9aa7d659ef2102b213f858410bb2a356`

```dockerfile
```

-	Layers:
	-	`sha256:4b6e3122492dc41208fdb8375cdf8a0a6213c1ffa99a9cdeb2107d9e724b17de`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 109.9 KB (109871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb86734f65fd5533728477d81d74430c96dfaca5f2f788caa11f0fb71c27a03e`  
		Last Modified: Tue, 01 Oct 2024 22:19:21 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:935b77719672afe22925be40240afd303a0734d070ec91a3ba49231a08c238c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6752730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ba33e0e1337b182feb5bed7168ad9afa64f9d6bc647fbb1b074b73166f3292`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc4dfd7ae560ea0456632f4beafcca7935451b4a359349041b60b7c4b29a38d`  
		Last Modified: Wed, 16 Oct 2024 00:57:23 GMT  
		Size: 3.2 MB (3179977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e627d10f556f16802c0693444991049eaab2e4c28195697d2b85cae15424a6d`  
		Last Modified: Wed, 16 Oct 2024 00:57:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d5156813e46a9893f872c702fc20d623e731e3e72d1f1c9ddaf0836772cd5c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ae86c40691c7de1f736529712145bc5a47ece7aa4765ae49650a7f3e403628`

```dockerfile
```

-	Layers:
	-	`sha256:97d6710f8af563b4404eeba221ed076b0acb9d4e66892ce89b00f371cf72aa04`  
		Last Modified: Wed, 16 Oct 2024 00:57:23 GMT  
		Size: 108.0 KB (107976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc808543234ba9a2eb31c873b788d8cf820eea7ef0f4e96eb52c3994e34e0c47`  
		Last Modified: Wed, 16 Oct 2024 00:57:23 GMT  
		Size: 16.1 KB (16115 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:384459795544742c9ad20f715baae9ace6b1776b781c4754949c4637cf4ee210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fd0c18e093ce21a8c43565b5220252c4d6d448f80d02cd1bc28f4f381553ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07fc64489ab73e21a5af01146fd448a4897bc3589564f82c2e2835e24a10a2`  
		Last Modified: Wed, 16 Oct 2024 02:15:28 GMT  
		Size: 2.9 MB (2857236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e320db5490bbbf64a75ed42a68c129666a90ef67188f51356450b3c88fa816`  
		Last Modified: Wed, 16 Oct 2024 02:15:27 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7d1a7a9a4a60e7de81aeb1bff1890aa6e5a9e14bcbd2dcbc437c4aa743a91aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b3262215f71dc39547daaa3dd7cc25bda5ed338408690ab0a1cc9346741ca0`

```dockerfile
```

-	Layers:
	-	`sha256:d9953b421b55ede406d6907bdccafd74b1daa5ec98da3a2761a3689a3b4a743d`  
		Last Modified: Wed, 16 Oct 2024 02:15:27 GMT  
		Size: 108.0 KB (107972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be9a1996c7ccb8812224b53be12a0cc668223aef590dc0f6fddbd98790338565`  
		Last Modified: Wed, 16 Oct 2024 02:15:27 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:56a4334f264ca3c863c20dee720fdb7340c8972afc4eb1dcd544481cbda73c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6468319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd8b659a0cc2cb30e4502b78052608e8ede8d9faa050692322999a8ac9f3748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_COMMIT=5edfaa45e791bbb2bf6c9342e13e5e364ff87bad
# Tue, 15 Oct 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20241012
# Tue, 15 Oct 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Oct 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Oct 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8304e7c76877c22906cb794525f5c1114c175fdb813176799f4934b2daf3ee6`  
		Last Modified: Wed, 16 Oct 2024 00:58:42 GMT  
		Size: 3.0 MB (3006386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dba904fe386dd05dc99363d36c7f68f5e4cda765187589617352e9625326339`  
		Last Modified: Wed, 16 Oct 2024 00:58:42 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8e84e7b126ece61a93fdfad392b88ea875dd5b7439685063235c2034d7fc8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 KB (124019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aa252e0d6c1421ac376ed413db5faacacc33e10a3307c8ebc67cbee66e61d6`

```dockerfile
```

-	Layers:
	-	`sha256:2da768231046665df0bad76b6ce60306fa05929bc32a081744cf6b5c4adac86b`  
		Last Modified: Wed, 16 Oct 2024 00:58:42 GMT  
		Size: 107.9 KB (107942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f5ae130e5ce222708123b6459e686396dc2f0446e9dc572a5eaa3066bf1e35`  
		Last Modified: Wed, 16 Oct 2024 00:58:42 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json
