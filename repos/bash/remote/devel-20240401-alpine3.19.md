## `bash:devel-20240401-alpine3.19`

```console
$ docker pull bash@sha256:cf3e4f54a774e9a896512766aa94934f9898444fa50827370767d461e6e7a41b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20240401-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:1ba2f8d5524ff6abffea0d2c7f444ba05c3dd0ee0b065599d8b6af44c8d12564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6285433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7593fe784890dabfcf243e9c828e5c1117bf3a5dcdf158e4bd1a4ff3b0bca91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
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
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a07f0da994af63b3ffb86e1dcc3decfe143c209ed99a9544d80dfd76bda9fee`  
		Last Modified: Tue, 02 Apr 2024 18:50:19 GMT  
		Size: 2.9 MB (2876372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a089a8623ce49d6dec043b8d573683e0e28c3ea2cf89477238a7a2a3138adf`  
		Last Modified: Tue, 02 Apr 2024 18:50:19 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:f0fe1bbb678be009d104c5fbf27ebbaea58684a76e29f48899cfd07e0faad549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151ec55103935aa0d739896f50be07f8da09a2696777073c88dd343f20e72b48`

```dockerfile
```

-	Layers:
	-	`sha256:7cff39f75106f9b281d576444c3ebbcecc20efe0c851b9d7b66376654084fc26`  
		Last Modified: Tue, 02 Apr 2024 18:50:19 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cae00c20200257cb6daccb2a6d970193ee511493994e057473a9bc430576e86`  
		Last Modified: Tue, 02 Apr 2024 18:50:19 GMT  
		Size: 16.2 KB (16216 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240401-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:a28892b447032c2970ce75262c7d0df3ca77ee1b21e9bce905cb939a76e99692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5994212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba115b12bef533f9580b3f918d58dd56c954a264c2d4554788957289e30bf21`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b76b6c65ad48be3d8174bf1da1ee29ae0aea838c250da846c45e62424bfe6`  
		Last Modified: Tue, 02 Apr 2024 20:41:02 GMT  
		Size: 2.8 MB (2828483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c46771bcf0e3cd0fd1acde956ad1d7f0ea3156767be8c2bd92d98447926b1ed`  
		Last Modified: Tue, 02 Apr 2024 20:41:04 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:b526858227c7dbd479d3e968c369b8ce35f53690c241712a9fca7b2af7661395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d7980f8fa41a19f86d8814623fb9e9a13d5b2f608e7c8f26a2ff11b1d8bf34`

```dockerfile
```

-	Layers:
	-	`sha256:4c9eb1e74f58d36a25ebd6aa3ebdca5c4239deb6e757908755267715296e0942`  
		Last Modified: Tue, 02 Apr 2024 20:41:02 GMT  
		Size: 15.9 KB (15905 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240401-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:ac8c0d7225e1bfba0e0eed3f8dfc52386f6e01901babd29560ebd53554847688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8dc64fd970cf1373db09dc4088f191742fe9cf9555606e96a676dff072335eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
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
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fb5d022b435654aae8a26ef0fe2396cd7621f3aa95ef6671fed4c347c28796`  
		Last Modified: Tue, 02 Apr 2024 18:50:45 GMT  
		Size: 2.8 MB (2773315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961759e2bc01cb3920199cc6b5f49cd54448c8d870ef3174b564b7254d96577`  
		Last Modified: Tue, 02 Apr 2024 18:50:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6964333afa1c72a7a4e648e38834d3a32c17a5a7e3fbc15de9b07c4833bc8157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62d15c289dea46fb522f7300fcb9240730ff94175dd5a679b6237b9df8f90811`

```dockerfile
```

-	Layers:
	-	`sha256:6d6593613cecb6d17d00f4cd8c56035794a57a6cf050b0cc4f34e069b742ada0`  
		Last Modified: Tue, 02 Apr 2024 18:50:45 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1888adf08a84c191ebb0b42956558c275a905c375830f4fad5d9ef552d9ad48e`  
		Last Modified: Tue, 02 Apr 2024 18:50:45 GMT  
		Size: 16.1 KB (16120 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240401-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:4b7e2c72a25f2dd149a1d05e6efe1fe724fa67258bddcc71276d1aee34c74d1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6327505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265d792a2c565ea649fb49d1c3af2b7e02ef7e96755d0dd85a3f925960e0a922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
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
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729f24129acb4eb7a02dceeace5d3db837df9abc7b183b70d26b9cc018e10339`  
		Last Modified: Tue, 02 Apr 2024 18:52:00 GMT  
		Size: 3.0 MB (2979456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263aa3e5a2720fe092be74208ddbc8d94d953e3ed282db0d9cd0a2c70a254a1d`  
		Last Modified: Tue, 02 Apr 2024 18:51:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240401-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:acba3dfb959d2e8b028659066e66623dd33b8cbd1f400608fbd13cabd88339af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ff4562758cbc4ed3fbd501b66c2b6754271c2a849a3ab58087015f6c708bc9`

```dockerfile
```

-	Layers:
	-	`sha256:8acf147da37decf3f8e0a01bd8a9cff4804bb137d868f8d2bfd658ca2200db13`  
		Last Modified: Tue, 02 Apr 2024 18:52:00 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe654c5e8b7f32e4f18c2f449409d3e9a9bb1749646a1203527ab199ec856f80`  
		Last Modified: Tue, 02 Apr 2024 18:51:59 GMT  
		Size: 16.1 KB (16060 bytes)  
		MIME: application/vnd.in-toto+json

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
