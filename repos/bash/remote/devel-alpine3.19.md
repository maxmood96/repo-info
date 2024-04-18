## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:16779783f5c1437baf69cadf315f1a751ff6a2677fb30c08e2b7cf59313580eb
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

### `bash:devel-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:7137a42dba25fd4b160b7bff6dfcbfb0c0f24bb0eebb6df004087dbf5dfdf801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df5ff6239a6fec06fa04a6cf7c44ed815899c33b4495db9ecc8d396bf828f77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91127110982a22618b81bcff7dbac9ab649b7e409989b538fe6f4b56e70e2f6c`  
		Last Modified: Tue, 16 Apr 2024 23:56:57 GMT  
		Size: 2.9 MB (2887640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1e253529cd9d200bf8df15c2e528225107022673688372f075ba93efa81586`  
		Last Modified: Tue, 16 Apr 2024 23:56:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:5f68a0f437d8f1fbc88f6dfeba1b24ea7fb1f98c8790e938ae9d8cf338296bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72de0a7400cbb6b70ab7f6b40bc3c3213f9b1dff56add0320ba474a72f36e02`

```dockerfile
```

-	Layers:
	-	`sha256:947036afe5b7e60820072ef5884907df4bd6dd5b6827c039d5b8d355a2b63652`  
		Last Modified: Tue, 16 Apr 2024 23:56:57 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4574fcba169f43e0e42c7985356d4f5e04553d031e6f24581f35462cfc42bf5`  
		Last Modified: Tue, 16 Apr 2024 23:56:57 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:3d5b19b424084910582441cab17f1eeca3e65c20a3cba1a0104386af57bb1ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6005213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee519a49a6cdc62d73ea7a1e1c28050abc714dbc8f8bbd28c29fd7bcee072a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbe07e0285c8841240363e1ae76c027c5710235429b6a0e96149348b811f4da`  
		Last Modified: Tue, 16 Apr 2024 23:56:48 GMT  
		Size: 2.8 MB (2839480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ebc632329e5208cbd3087412f657db82f3da64ce3428cf4f497a837f41183a`  
		Last Modified: Tue, 16 Apr 2024 23:56:48 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:288d273863b16ce54ca7228713860811a91996b2896315298b9c388a04d96bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68df90938f75a23c0f8eb1813b4d551f8c4c55f2a39d06e2189a801a64f64ec7`

```dockerfile
```

-	Layers:
	-	`sha256:36e0c1cbe75080185a9d14ca18e33d14fbe971a91b20912461826f7d0b0cec7d`  
		Last Modified: Tue, 16 Apr 2024 23:56:47 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:827a88c9b779e6fc2c83e8d212c285670e53c6519d300abff5bc48aaa37738e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5703331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ae18885f3f24157de9f0291dd8376af36d2fe9e068ac8b0f824baf22741f22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898806e9c0c936eac56ed40d3b32a51cb826dd532e4f011a1bf529f62fd59035`  
		Last Modified: Tue, 16 Apr 2024 23:56:43 GMT  
		Size: 2.8 MB (2784098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03e721764b97a7ae99d27dbc27be484682dbe0dea8b6d565f85e54a8fc55725`  
		Last Modified: Tue, 16 Apr 2024 23:56:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:669f3252de4cfd455fe450adf147dc8cde4cbe26fdb270605b7c7676dce2a29d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7f4c6db1f9108e0ffddf7ef1f5c64d2165e157e85aa74f46aed092539eb582`

```dockerfile
```

-	Layers:
	-	`sha256:7ab8696e5e9955deff8e6f15e06c8128ce2d4c4779d6fdd3e8dc8651aeb282cd`  
		Last Modified: Tue, 16 Apr 2024 23:56:43 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2e70bc0a38204efc1a5ac0f5ea3ddc216ed44675592ec01a6080cdfcb8c783`  
		Last Modified: Tue, 16 Apr 2024 23:56:43 GMT  
		Size: 16.1 KB (16080 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:90b3572a7ea98f9fd1e9b32cd44883c25bac457d7c69f296b143f2d57170a2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6338044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a0a080e4a7e65e16782ccdb9329f1b46c8ec2f8c9d7052a9f7ff2c759de1f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fb178bfbd75f72200c72c8d79064e38947dd67b4d0637172d9c6fb0d2256b`  
		Last Modified: Tue, 16 Apr 2024 23:56:41 GMT  
		Size: 3.0 MB (2989999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadf1799d8be6e92c259dfcdab5e98b5b350f96a72607ca8e9a950fea91625e4`  
		Last Modified: Tue, 16 Apr 2024 23:56:40 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:056a8cbab1d994d65adb1c6784fb3370638d19a3e186334eb17048e6b96fe7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 KB (126489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9a2a0a08510477681dc59a42df07f456ba4b160eac2b349c7268646e330e43`

```dockerfile
```

-	Layers:
	-	`sha256:5bfa363076ab429835e49cc82c4907ab1da968ec5b187b317462711273c1a2ee`  
		Last Modified: Tue, 16 Apr 2024 23:56:40 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f914f25380b6608a0bf74da4698815267430f47587d6525883567449792aecf6`  
		Last Modified: Tue, 16 Apr 2024 23:56:41 GMT  
		Size: 16.0 KB (16020 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:e995fdbfcf76ebc83d13e70dbaf294014710d5d83a2d7d8bf6dfa8a3d3d7a4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6071650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363a93767f8cb5b365575a822b32495be3455b0c378aade75ad9e46049e4b87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce2247ea4f1b5a734ea1c4a43ff075ad061c194cf93f23a541bd05796fee842`  
		Last Modified: Tue, 16 Apr 2024 23:57:00 GMT  
		Size: 2.8 MB (2827224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17016b74a654a42a75c48cd9a92077e43e96ec9d2c0620d71287c4f2b16ddf65`  
		Last Modified: Tue, 16 Apr 2024 23:57:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:e2fb6afb106c1dd5ad24971cae48df9670bade10a318557d7f3f813bb299c2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 KB (126580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d12ecc8721c2752fbb769667736952ca740a66a0d2894bbf0b9f80bd3c4009`

```dockerfile
```

-	Layers:
	-	`sha256:840bd31c8f9e5cf4336480ce50205c5e0f12de88108e7f1c231282a52c159b1b`  
		Last Modified: Tue, 16 Apr 2024 23:57:00 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ce59f004130b7f215273666ab1dba22851ed7077fbad337459d6715b02c1b7`  
		Last Modified: Tue, 16 Apr 2024 23:57:00 GMT  
		Size: 16.1 KB (16147 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:f3446304c137f8f370f7488232c8ac7c80bb1a38cb0206057f4f1d6939a3d581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744f73c60deb11b36517ceab26e577ae90a0ce2f7a44519d472ecb5693f60f9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f4d87a1111077b2304b70a4cf7f241594065e55f64815fb36f8ab81d54c9f6`  
		Last Modified: Tue, 16 Apr 2024 23:56:51 GMT  
		Size: 3.2 MB (3159780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2386316f7e22144455e8e601d519e2d37788fbd5d5d4ef1c8135ceaf6f16f0f`  
		Last Modified: Tue, 16 Apr 2024 23:56:50 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:4ee7575e78b52db677abae433156db334093cb73e2991ab07d3a95b8e727bb19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 KB (124586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f44ccc36715c43ee999f9473ca248f431d043d6bfccd8c9866153764e2a063`

```dockerfile
```

-	Layers:
	-	`sha256:eecbaf551869360b8100b0ecce6d4fc852c2b61075b48ce531cdce2e859c535b`  
		Last Modified: Tue, 16 Apr 2024 23:56:50 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afccdc74aaed3f574db7f83a684372ec4f235d450fc9282c2f2701f446eaa163`  
		Last Modified: Tue, 16 Apr 2024 23:56:50 GMT  
		Size: 16.0 KB (16048 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:7cff640a6c18804b90e9aa23264b067e3d104d37d35a52c8a4b4f4178c2491ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68dfb75f54ec4a7372e0892db064e307e4983a43a147fb375de716169362a443`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_COMMIT=a06616a689a239e0ade2c08ae78fd114d2324c5a
# Tue, 16 Apr 2024 06:58:57 GMT
ENV _BASH_VERSION=devel-20240415
# Tue, 16 Apr 2024 06:58:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Apr 2024 06:58:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Apr 2024 06:58:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce57a71410539e5d0efe3f6de9237b5531299adf51981bf8a2ac53124b17d67`  
		Last Modified: Tue, 16 Apr 2024 23:57:56 GMT  
		Size: 3.0 MB (2989325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7002a661abdb53fb9d0ce4734e7dfe1a0036a3b85c5d80387e9be579e205e093`  
		Last Modified: Tue, 16 Apr 2024 23:57:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:d92857a56a48b6b0ec2bfc276ff95778314a53504219db6cc420a8cdaef4f705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 KB (124514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0c63e017b6a4a4b96bf07df626e4620013b3b3a1a098243e49f8080a741deb`

```dockerfile
```

-	Layers:
	-	`sha256:09ecdab4a7b8f063c84f028d8f701d9bb65f48588ec5056796e29bdea616cd20`  
		Last Modified: Tue, 16 Apr 2024 23:57:56 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291db1c0c80f8d36e1c706bbc2de37df0d63e1b07ddb8d667b208fd593342a47`  
		Last Modified: Tue, 16 Apr 2024 23:57:56 GMT  
		Size: 16.0 KB (16010 bytes)  
		MIME: application/vnd.in-toto+json
