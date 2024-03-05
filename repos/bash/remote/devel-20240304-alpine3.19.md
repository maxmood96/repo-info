## `bash:devel-20240304-alpine3.19`

```console
$ docker pull bash@sha256:33f28c12dfd461e36e691e526f4abd3a99ad61106dd3a48fc7923bb633e0a23d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240304-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:1d3017bba385ba5301d9b8938a1afdc85d64db1d9dcd5a47f3127cc65c4cb6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6057757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527cc0a3afb1c3a37d7879f98dea55ffc9b3dcc080c0feefa5294c86d11ce21e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af798975e7b55e62f30bf7f40df6f9726c5a8a86a658492cde7240e30819628c`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 2.8 MB (2813334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a9c6784cee5e82e1503f386263304fe6ca8faf59743a037cf2d57ac7c9fdb6`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240304-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:750a505b5e6d718923ce4d9621118317148e0f108a4201fdffb8748eb66667e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4c68819f189e0482858ba23a29b1345450afdfc56ce10e64f4b35c6152381d`

```dockerfile
```

-	Layers:
	-	`sha256:a6e7719f0b943058b3ca2fb8660b6afab5f2a28262cc147a4b5312595a15deb6`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa50ac30e8179acdef3a8837a56737c3b01adffcc8ea168947f54215f68ae68a`  
		Last Modified: Tue, 05 Mar 2024 19:49:09 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240304-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:9be587026993a40550d302be35ba241fba6bb3398e9e2cace469d2ab6905829c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6502955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138a21e605f88903aab696f244245bf9d83a55826b023263d43e145921ccf2d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526a0dd8a562e178a521176ca8de66e135ea756a83b1a03686f67e055cb093af`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 3.1 MB (3144266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f0b58760696b833488e3aa49c09a9c4a7a25d0daa8d41be78f2f7157da66e`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240304-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:7d77e0801647afe4cab566336af0a2f1791f31170b5ffc1f0e9e43156d5b6bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c46c51ef93ebf1fe3f5194cf41cf7d4539858042e662e12e1a981e921e02111`

```dockerfile
```

-	Layers:
	-	`sha256:a590d19a451ad9e1c2bc8878816500d9b0af26ab6636eccac3457494cab2ae80`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f46af97544ce61f7505f6a8bdc1fd9681440ac0f6a1cc29eb0051bdf423582d3`  
		Last Modified: Tue, 05 Mar 2024 20:11:38 GMT  
		Size: 16.1 KB (16096 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240304-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:71b24b6b94c39795ff1e0c814ba50f75217f86c496744cf5aa11a23dc9d32f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6213936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a717b176e12b35d33ce41062f06a94cfd200909d9c315cf2992a23180844754`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_COMMIT=54f3ed2278025081f897b9bd958fcf099fd5be18
# Tue, 05 Mar 2024 05:18:08 GMT
ENV _BASH_VERSION=devel-20240304
# Tue, 05 Mar 2024 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 Mar 2024 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Mar 2024 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c4427d40245c21ae93d97c5edc31a68c299265c802414845b4b9474212024`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 3.0 MB (2970968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af49d10815172af409e369295c3632feea3c10de39faee583588ed6741df965`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240304-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3280529b64231fcb69142f7088377a56f75e7d711a3539c3a6607f931fd624ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2589ccf6c7efe82b3c6e353faf622db5bda50cfc2ccdff6d9618d32d8ff7140`

```dockerfile
```

-	Layers:
	-	`sha256:69fe56bfa426a4c974e95cfa067d3de4d4292c8e10b8a6f8476c2270463c5107`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94e9d360667c194a71174dadc15ffb15cdaea42cb331dafc46f534b66622d0a8`  
		Last Modified: Tue, 05 Mar 2024 19:55:46 GMT  
		Size: 16.1 KB (16058 bytes)  
		MIME: application/vnd.in-toto+json
