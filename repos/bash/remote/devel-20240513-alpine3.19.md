## `bash:devel-20240513-alpine3.19`

```console
$ docker pull bash@sha256:84f0b5a03c382ff5ba7ff9832ee9dd8d5672fbc33c0b0ad2fb1889e59d40ff1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20240513-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:4dd1821c9f1a619825fd658ef2e1134166781fb3fbb532b0a985e21f290d055a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6301116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe598cee02d799058ea8db5c7f561df287e04b0049992d6892da32d955f3f0fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9032a2bb1a73677beb3edab366203ffbc5d1fc21c7cd5807a0fa1a4aa893fcda`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 2.9 MB (2892055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c822f41afd67251659654dae451c33bdc68fcc5bb04cd3a6539f463809a63153`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240513-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:73c2880a39814d70cb932bd77d872b7d177bc0b1301212d542f74e65f085a070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 KB (126958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b9ebb08a1e23397314dfcaa13e563cf33441c9a275a9ae3cbcd9c74fd17f7b`

```dockerfile
```

-	Layers:
	-	`sha256:e2455f8b0c77345a543a8f22fe392422abf5531699468d132cdaba05f1aba99b`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40a4aec2f56d1d1b8e7edee762abc5a3b2e9e0cb772d6714128dd54250f8e66`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 16.5 KB (16500 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240513-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:b26e020a680da6ae182047fa18b849c6d0eaad6809fd98b274f76d299260e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4199aeca6d1294815a725b0b3c2215faf160fd69432e2f200360dfe72a30f2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12a1cd85c93b804e59a8b47fcff957bf603e4240366e6150692f566aec7652`  
		Last Modified: Tue, 14 May 2024 22:02:07 GMT  
		Size: 2.8 MB (2843075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b397aa128daeae30575bf5ecf931741d3570d8869c93902b818faf3941cdaf`  
		Last Modified: Tue, 14 May 2024 22:02:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240513-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:fce7a04e3ce8ea4dbc00cbb79986c5037df612e8a7db615a4c5da030e3b48c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 KB (16351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1be75df2bcec4b270b3b5e0ac426cc3853c8230205510abe6e56d2b01588413`

```dockerfile
```

-	Layers:
	-	`sha256:613b5570f2ee86e1dfa008a60be457bc7b8fc7c325aac56b39270aa6b277c8e3`  
		Last Modified: Tue, 14 May 2024 22:02:06 GMT  
		Size: 16.4 KB (16351 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240513-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:d50a770f2c8b1338062b02010c60179bc42dcb23837b4f56c62737888d17f38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c50b385d383b0fc278141fcfa7f79860401e50221c3ed90811603ecda951cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050a8ae88d0380c139c902d002c87f1eb78d767d55cf735e68d10d85e835020`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 2.8 MB (2834616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7910573c4bab0c8210bd42efd7614575b4ee40aecdc42758c24b8f1da85a0`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240513-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:211d6af4a10c961ab0507e00eed4a6c839be9f3c5cb7613994bb0d67f8db07fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 KB (126904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a9430a7c79ce8cbbe2531518dae838763f3bbfb565a223d9d217342b3a07fa`

```dockerfile
```

-	Layers:
	-	`sha256:a9b2d00e9ef6009a7372f280da23f0cfa08089853a7ec934e096ea466bf8dde5`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b2a0770ea4d6cbf80823a6d0298af625079b422c39e0bca6c06724de9bcd72`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 16.5 KB (16471 bytes)  
		MIME: application/vnd.in-toto+json
