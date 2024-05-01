## `bash:devel-20240426-alpine3.19`

```console
$ docker pull bash@sha256:6494372981d9370d4c0daab5d27ea07a2ee45c0ecf6a7b83c4de074ad8af74b9
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

### `bash:devel-20240426-alpine3.19` - linux; amd64

```console
$ docker pull bash@sha256:0418e8df16078df5761a15335f115cb348814c950ffdf7155bfe68c70d45e74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6298426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc380ef8a2f4b025ec2292ce5ca0e5fa85b733f54caca72add02a5ff437545e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c3a071c1b715a4ad6d642d6def8431afa53fdb34505d498e2be3620e45613a`  
		Last Modified: Tue, 30 Apr 2024 21:50:28 GMT  
		Size: 2.9 MB (2889359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d0869fa8452453425ec21a1591f369487ba0e6f8d5be934f703f2ed85d8709`  
		Last Modified: Tue, 30 Apr 2024 21:50:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:94f3ee86e93afac8e0a1ed29de4b02c5433465a2ad6d27b0a3e53a9d24654908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da8385fd55dd9d523bce319183225e9a3af6b0e522c7029b199f51cdea87f7`

```dockerfile
```

-	Layers:
	-	`sha256:adeff06af4c62fb2dea5fb2ebc6191d53b2fa3520597ba4d75abfcbe22ed51d5`  
		Last Modified: Tue, 30 Apr 2024 21:50:28 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a458493174a5cf48c1a52533e42e20dba06c6756a8301a4b3b62b80f81b13e75`  
		Last Modified: Tue, 30 Apr 2024 21:50:27 GMT  
		Size: 16.4 KB (16380 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:23b369fb65d0ffeefd82e53044c1db59addaab6ff3979a994d7b8fc570a0ef6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6006644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ee7391a1af327233cf4fa21a16ffdd859263d1243d63f39f587995cd55fb6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9957f7abfebb695ec75ae56bbd9ec1f35d1f9b605dedf000c696673c142b491`  
		Last Modified: Tue, 30 Apr 2024 21:52:50 GMT  
		Size: 2.8 MB (2840918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9b396debaac11c2d326656b81d9f598448d3b6db1043cf68f817c14db20c03`  
		Last Modified: Tue, 30 Apr 2024 21:52:49 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:85c8417d0a75636c11c514ec772ed4b17ebebd08cd6269c10bfb2dec33a9eb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 KB (16065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab674cf8ced0e4ebb80a3869314c7c80dacc128a7ca7b5142eebaf15261297b`

```dockerfile
```

-	Layers:
	-	`sha256:870509d9597c52642f04f9ab7cc9c7f999c252210652fa56485b89b773c83ea3`  
		Last Modified: Tue, 30 Apr 2024 21:52:49 GMT  
		Size: 16.1 KB (16065 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:1440f822a74c0ff7a04b8c3dbf95fcdb13c516db1f6f159e2ad443c703705917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5704275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f539c18737ca71c7c250c49774335a72c64c5001f1be34f601af56a4907720`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bf534c43de9a179a15a13934caa971db723801386f4c856d72e5d31a14cc07`  
		Last Modified: Tue, 30 Apr 2024 21:54:58 GMT  
		Size: 2.8 MB (2785037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5950dcb4315c94d2520f9fd8d7d0c365ca30e49eb6c9106fd0e62c26f6e57246`  
		Last Modified: Tue, 30 Apr 2024 21:54:58 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:938e78a72933201b82882996c9fa3b48635befccbe19e052a7f237d3fd6236e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ccf227056403d7b61df74a17c3cd66b112c38a9ced0ceaf5230432c9f69496`

```dockerfile
```

-	Layers:
	-	`sha256:4f121db3e9e76addb9902d1c0b01cb6d9ae40177f1987639387040cff0051989`  
		Last Modified: Tue, 30 Apr 2024 21:54:58 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcfb0d7106c654798da1a4b12454b4daa6345c4cc296b03e8eaf396168dba44`  
		Last Modified: Tue, 30 Apr 2024 21:54:58 GMT  
		Size: 16.3 KB (16284 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:a9f0bc44d4802eeabd3db6e311f2325aac197b294346fd1559de49afb7f694b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6339811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382c4d7294297ed83d98c281d434077ac73a3bb0c725375c9f9d5a3fcebf0030`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f903a3b178f577765ef59643df5f0fdf3f09df18b425024b522a3241c7f5b80`  
		Last Modified: Tue, 30 Apr 2024 22:09:25 GMT  
		Size: 3.0 MB (2991765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1109444ed5b65f955f97992563dcc9ffa5a1f45c434dc73688d93513299d99`  
		Last Modified: Tue, 30 Apr 2024 22:09:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:2af2f3fbaec6d1ff08e7e8a9255e22bb4c9afc8fdb289ad0fbf44c267bcd3cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1822d489c074be67dade73b35fa85e7f613712d7ece2050a9000c4d439e4486e`

```dockerfile
```

-	Layers:
	-	`sha256:f0ba731a152d4d12080306101b879eae55118e64c984b3aba0e6fb1f980476ba`  
		Last Modified: Tue, 30 Apr 2024 22:09:25 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69e65d3595a60e200af6ded7569b8411ce68ba46d7d17a645672054fbaa799f`  
		Last Modified: Tue, 30 Apr 2024 22:09:24 GMT  
		Size: 16.2 KB (16224 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:da20ce4a789bc9fd2b0cee8df582d1f03855ff821fcb87142e816aabfb17b913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6074982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a748f93b76142e2aec874f6459c9e9f7e9b75410ab3a9bf19586eff112c0b653`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6251078e34f12e31ca1454e8c80890e863fd1d40ccd39e2b2b3c24922c318f40`  
		Last Modified: Tue, 30 Apr 2024 21:50:30 GMT  
		Size: 2.8 MB (2830560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d54168d8e8d7e4f6f2471e135e984811b908eb655bab50be6d7df7c1e1f304`  
		Last Modified: Tue, 30 Apr 2024 21:50:30 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:3a23f5483c1a961fb5277a6a648196e7772fa8690c2498c2a04e5ba281dcf7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf3ef8cd064b1fa37337e1e3a90207ed4e653d3b62521bfe8113ede00ca1eb5`

```dockerfile
```

-	Layers:
	-	`sha256:225e7d3caa9aebb6282534dbc0376ef05f20b6f6fa1286d3b97646ea1dc2bb3f`  
		Last Modified: Tue, 30 Apr 2024 21:50:30 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3e33d3af6dadfa8f90c429a8dc0877bb6ad89eb3a8d6f3da872bf2afbe48f1`  
		Last Modified: Tue, 30 Apr 2024 21:50:40 GMT  
		Size: 16.4 KB (16351 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:e5b7ee25921445422542de4add917e3c54a9422087d2e86bd10f3bc411f4ef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6520799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b75c801e5911d9c460223153ceaf1e945d78c1f47c51b4d19e6c29548b200a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6491c1ade01bb1809c60660277a660f3915b55b3c82c7b2df4cf8b97cb0471`  
		Last Modified: Tue, 30 Apr 2024 22:04:05 GMT  
		Size: 3.2 MB (3162110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf7f9e47650baf3c444898bef40511bcbd84aa2b34a1642dbe598a562d34d3e`  
		Last Modified: Tue, 30 Apr 2024 22:04:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0291cb4b3681df39429348fecfb8f31a009791d5afd33329c82e1b576dc674ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 KB (124790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1ccb2d0900d94aa76f030599b8356afd9e55e441a973b014f1bd61f82ff6cf`

```dockerfile
```

-	Layers:
	-	`sha256:4f06a8c3b141458ef300ff4a50cdf5ccd496460af71ce5fccc713639aab12a48`  
		Last Modified: Tue, 30 Apr 2024 22:04:04 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998ab747eb48f11a63de847707b50b9fb0614f82785d8ddae263000c5f3b04d4`  
		Last Modified: Tue, 30 Apr 2024 22:04:04 GMT  
		Size: 16.3 KB (16252 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20240426-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:0f12ab296f2f603d265f6211b0f09f23f1497384022dd9651ec5763e261820d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6234646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfd665b8e319f4890fc472093f6040888bf52156c7b3f4bddf3f0be6a973c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_COMMIT=9c430f6bf37984e01977cc17f7066a6498aa4f18
# Tue, 30 Apr 2024 04:18:16 GMT
ENV _BASH_VERSION=devel-20240426
# Tue, 30 Apr 2024 04:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:18:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:18:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4bf4af45236ff2e5186391297a2283e55891d6f4eb9af60d777a79262b233d`  
		Last Modified: Tue, 30 Apr 2024 22:03:43 GMT  
		Size: 3.0 MB (2991673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c888256cd97e39a7a25eea9b1abc7467aa0c451cd076f6eadea2d36fed868708`  
		Last Modified: Tue, 30 Apr 2024 22:03:43 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20240426-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:565206aaee0b3d43487bbc70b3e00ef9b15d94127561a34e0eb1458e4570c537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102ca2f1fec9df97fa77200466f322aa44ebe9244455874deab4a3a337fc1445`

```dockerfile
```

-	Layers:
	-	`sha256:36d154ad018ab595ec80a612843db4a92f20c55e17879f301e6582f33ae3d3bb`  
		Last Modified: Tue, 30 Apr 2024 22:03:42 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25cd6034bc59850820ab8ea4b0b8157330357547d7d8ca6cefe8dccb3cd1925`  
		Last Modified: Tue, 30 Apr 2024 22:03:43 GMT  
		Size: 16.2 KB (16214 bytes)  
		MIME: application/vnd.in-toto+json
