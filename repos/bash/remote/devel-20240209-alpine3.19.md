## `bash:devel-20240209-alpine3.19`

```console
$ docker pull bash@sha256:635fd55a571777cff6b459f4a10341b65ba661eaeec42636925166d2bcf610ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20240209-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:2682dc44559c8b6caabdbc2c1e1b7a4471a2298a82f4fdd09930e9eb50184867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8a89b57a14bc81340b6652aa95f21ed49d036ec5405738f16436d791c294b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_COMMIT=fbc7d97de6c6f3dedb34f49f89a628a99ef6ddf5
# Tue, 13 Feb 2024 05:18:07 GMT
ENV _BASH_VERSION=devel-20240209
# Tue, 13 Feb 2024 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 05:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 05:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff349958c97798d90a3040c575724cddcb7ebff843e5470c8cad191ba0e3b82`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 2.8 MB (2808363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409bfa5cab51f45aefd476e0e5d6378551b6fddb82263d0d5b7a273cc41e024b`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240209-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:a690ff6c521ef80d47faa731dc1dbfa84815a3f6403bbe9a9094d5404a4bc02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fe2573fab3179eb27181449339a173ab604ef0ed435017c36da93bde393962`

```dockerfile
```

-	Layers:
	-	`sha256:2c306496299bb7d14b26fee1d15bc4b8849c38d1a275469adcef5511d00e228f`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 97.7 KB (97713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f418bc7197c235d7b6752234db65a2b33fa3788e9e370b0fdf30b8ea1e4b25`  
		Last Modified: Wed, 14 Feb 2024 19:54:08 GMT  
		Size: 16.1 KB (16139 bytes)  
		MIME: application/vnd.in-toto+json
