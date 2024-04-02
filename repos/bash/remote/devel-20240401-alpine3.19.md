## `bash:devel-20240401-alpine3.19`

```console
$ docker pull bash@sha256:26e40aab6aa657652e7cf6a291711648eeaadc4d911532f45b37ce14d5330611
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240401-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:b3b24fb98397354ac6f16b29485da7098690238a4c0327b19b1ff97aa12dc55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6060186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053cb62bc1de8a68be2f99f35d2e339fbd9ff305834c0596aba8855ce02f169d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_COMMIT=2532a2ccefc50e26a32ddd430286af6f5c43d881
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240401
# Tue, 02 Apr 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66733db5286fbe8531dbae7f0c745f3640b8d5c0248dcb8098e06ecf82ec1023`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 2.8 MB (2815763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e52512be8797e030ff71721f7954015926afa9de168619d6c9cab14c64321`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3a75988c7ef5b5c5d182e34aedb0a6b54117a4ccf1e1b02795629eafe95c4dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335174ea1f2b4a11b4ddbad36711ed3ea5df9f13eac22a353f74a20648286b8`

```dockerfile
```

-	Layers:
	-	`sha256:75745f73b9bdf3f8fd79e045ac3ef8a0577402104b296c8d0ebff0062f5a384a`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f7cc8550dd446f71a8326bf3fe2dd381e0c920f4bb61201d1a02c42dd3e939`  
		Last Modified: Tue, 02 Apr 2024 18:50:15 GMT  
		Size: 16.2 KB (16187 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240401-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:b53c69c7a4f2654255744b08f4d8d9de60abae0a6ca18e89e549056805ff07ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6506675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8be5c35c8b6128dd4296cdb3ae8c2e02b5ca12bb8335f8c2311955102dab48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_COMMIT=2532a2ccefc50e26a32ddd430286af6f5c43d881
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240401
# Tue, 02 Apr 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a5bddb52ca738f636368520c90e8b752d7ce4c1b2ceaff149a9715f7b10e0b`  
		Last Modified: Tue, 02 Apr 2024 19:12:13 GMT  
		Size: 3.1 MB (3147985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347fa000a59abc68ed7b9d2899abf6335fdafbb91e74f46ba48cc6e04ca49616`  
		Last Modified: Tue, 02 Apr 2024 19:12:13 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:ddbf3caf2d0c570296a8f8375f3f55dec7050ab1a1ff5c36515459c8c3656c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3bde2e569a68dd268328e1cb278be848c7a4ab9148c081c1d47ce4ac13ce1`

```dockerfile
```

-	Layers:
	-	`sha256:83ff69941b147be96d491e6cdd09a3d41d1c336f2fc90c475792c04d32e58218`  
		Last Modified: Tue, 02 Apr 2024 19:12:13 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8271d6d60996f107fbf12487d00297d893831771525f8fd7efcd558d223c8c37`  
		Last Modified: Tue, 02 Apr 2024 19:12:13 GMT  
		Size: 16.1 KB (16088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240401-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:77df0d772d52ee217bc3c818bfbe42c3a209dffccc5bf8af1322422563d5d497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c36d6217f744cc61784d7abd7aae0c29b3dd755177d25318e33ad02bbf5c0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_COMMIT=2532a2ccefc50e26a32ddd430286af6f5c43d881
# Tue, 02 Apr 2024 04:18:08 GMT
ENV _BASH_VERSION=devel-20240401
# Tue, 02 Apr 2024 04:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Apr 2024 04:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Apr 2024 04:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2543bff7d2f54b2086b0286cb1c37a1ca700d15fa11cc1b2d88ce07eb4e87`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 3.0 MB (2978024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e10c1c0ac8c03737e6941ac492a7b0d9c24dabdca1ed809a0606af4141285af`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:16b2ba959f7f4763ef0e3222282145d29bff3685db6fb7e5d030198b8c7bb97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33805e19c2671bea8c2f56d836215f25a865a87ad78f5c0f602f037af0e38f2c`

```dockerfile
```

-	Layers:
	-	`sha256:6c45da99e0b55bb563c72199fc28815f17ba021cf165e22ef1813fd370dda148`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0563043058dfd078cacaab69588340462b94651a004addfb3ecf1339832997c`  
		Last Modified: Tue, 02 Apr 2024 18:57:09 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
