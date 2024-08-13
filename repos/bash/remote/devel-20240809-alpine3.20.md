## `bash:devel-20240809-alpine3.20`

```console
$ docker pull bash@sha256:0c20ad21b354fe89ac0dc0eca85301163df295b9f2bf7212f4f022ff47698116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; 386
	-	unknown; unknown

### `bash:devel-20240809-alpine3.20` - linux; 386

```console
$ docker pull bash@sha256:6310bcfe668760fa4f721f2e3889b577fa9a9068165d20d753c754e0f5b2138d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d45188c8e972f486d2740e14f5e78aa2a92e646f414c5db0c5401f33b44d892`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_COMMIT=772e7e760e8a098e4d8dee21cf11090be4757918
# Tue, 13 Aug 2024 04:18:04 GMT
ENV _BASH_VERSION=devel-20240809
# Tue, 13 Aug 2024 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Aug 2024 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Aug 2024 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c869346356eafc5441bd6ccaa9dd32f056bf4d92a557c2cf038b8bdb8b362bd7`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 2.8 MB (2845752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28b39f983581ec0adc5ab93b5447c0e90c9a4e1c6701533925c9b7879540da5`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240809-alpine3.20` - unknown; unknown

```console
$ docker pull bash@sha256:5ee575cd6a5df30dd190a69122a4863351fa5acb3a042f5173fd18be942e9a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e77a11fbcb825d1287ae9257e3b8e73aac8c3aeb413164e27443a11624b9e3c`

```dockerfile
```

-	Layers:
	-	`sha256:d135542e3555d38116f728e441e36b88cc32ea8eeece46d525463e078258a37a`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a4d1f11e073fefeb1eb9479659f63fc8c409cca9e8b7a9acd1873d8daf7f1c`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 16.1 KB (16150 bytes)  
		MIME: application/vnd.in-toto+json
