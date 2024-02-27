## `bash:devel-20240221-alpine3.19`

```console
$ docker pull bash@sha256:f7fe9433d3dfff564504c3d45b02c207cfdc37274fd33db20306c824ee33f777
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240221-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:4311cfd3cc4f243a47aec8e01e8d1c1a992e53021948fd146f2204c59ee481bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f87d164febfaddd444775757bf71f587c272adf1fb27753d395ad541b407a49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_COMMIT=43ecbeb31e5bbbc1a7557243af82b9f3e6390ced
# Tue, 27 Feb 2024 05:18:06 GMT
ENV _BASH_VERSION=devel-20240221
# Tue, 27 Feb 2024 05:18:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 27 Feb 2024 05:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2024 05:18:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67d54e3a5e1c67be96f3328ec949ec56ebd8020c1506e715e4dac6da39553e`  
		Last Modified: Tue, 27 Feb 2024 20:59:20 GMT  
		Size: 3.0 MB (2970156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c9bd7927206eb957bd1faaf241089c361eaff1ad0868559d31931db2c0ef5c`  
		Last Modified: Tue, 27 Feb 2024 20:59:19 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240221-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:65895b2b47a95554d0c64c95ef4e5080c079af4626228bf30ed80c7d59220547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d307d3baddfa45c8a5225dd33875417bc41593940876fef7f0045c05473956`

```dockerfile
```

-	Layers:
	-	`sha256:5370915c1c7ca0311c3a8fd0c3f8592808d5752549d9996b6ebf5e7295db34a5`  
		Last Modified: Tue, 27 Feb 2024 20:59:20 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c7fab48e87915bc14ae4053c83f74cc736f09a0121288c64c5763376e557233`  
		Last Modified: Tue, 27 Feb 2024 20:59:20 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json
