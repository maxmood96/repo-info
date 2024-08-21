## `bash:devel`

```console
$ docker pull bash@sha256:d344d8c2e7afba48e331c549a5f4a3b623c0a0d6073415fdace517bed2732c55
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
$ docker pull bash@sha256:1d9ee84d9c00cac945d28e6e8681c49bcc5a3541b9a2e0033213ba1b70cba26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6526339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a1e1bec1ac8b6b980c2432135778d65dea98bc27daa886410030edc0a44d375`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0a396941f56838bfe2acf081bfb124f1b6507af1bd2cd4e147144c8920f3f2`  
		Last Modified: Wed, 21 Aug 2024 01:06:26 GMT  
		Size: 2.9 MB (2903109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d912f7aba0e5e5622f6d5af2e7ea3a0c145329e2442aa44509ee87ae19f018`  
		Last Modified: Wed, 21 Aug 2024 01:06:26 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7db8bfd2e4169a4a7fd67a89306c9825e4db739822b1d9ea1f8c978d7c89dd0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.1 KB (126054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f6b054f53ca0b67bd3ab7454f227e1a90fb783e9d23770eb736b2cb490287a`

```dockerfile
```

-	Layers:
	-	`sha256:8459ef6f891d893415de008edfd965e12cb006ef67ca3c114b1566bcb50c88ff`  
		Last Modified: Wed, 21 Aug 2024 01:06:26 GMT  
		Size: 109.9 KB (109883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5142e9fc670a97201633ebb4bf8dbd9e86e2c4a69cf232bf5fc12914c327fd48`  
		Last Modified: Wed, 21 Aug 2024 01:06:26 GMT  
		Size: 16.2 KB (16171 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:c5fbeb9bbce79d4cfc121b75a85f362dd7ebd86b0bfbffd044713323bf81b2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6219217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451e021bbfb9b6b16d5361f5abbdcf22dbac4b52d2dbf6c782256ddcb93ee89e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d12022e1b9343db39cbd6f6933d8319240126994dc709e16ea54ff5b6dc080`  
		Last Modified: Wed, 21 Aug 2024 01:00:06 GMT  
		Size: 2.9 MB (2853695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1558bc8dd06c0c71a4e243edc26394d980e03079a5f353f98fdab7fd2e14f`  
		Last Modified: Wed, 21 Aug 2024 01:00:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ba21523f005bcb95724d21f3980a9ba20be909d019e26f28f1c6c5e7366fa541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46723a06038daf04410feba64dcbbdd94068f83a42aea20f039f8dd2f5651d3`

```dockerfile
```

-	Layers:
	-	`sha256:136a1df4f60cf7e9f5fe0548a645261dbec192994d5b7928092bd8782801bb4a`  
		Last Modified: Wed, 21 Aug 2024 01:00:06 GMT  
		Size: 16.0 KB (16022 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:65640ba9912e5a1ecae688e74104bd39ab8a7d2eeb2acf8377599c7d96a456c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5891694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e37da82f6a02a90351c09777e173c55c91990dd94cb62a7d1b674c7c5d4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fe50801ab2b27fc204bc176d8ab2e72d114294f3ece2cbe71b2634175ed2eb`  
		Last Modified: Wed, 21 Aug 2024 01:05:55 GMT  
		Size: 2.8 MB (2796398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f687c2135c073d7732f946ed22718f9014ade2a07142aaa9a07cdf95e8fb1c7`  
		Last Modified: Wed, 21 Aug 2024 01:05:55 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1aae1016340d4c3a3e93160e90d95fde61c409a849bb45eaf51dd43df94f85ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 KB (126160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e3bb917457341d027c7b74af453e111e9ab7bbd89f821dcf3ca31a0a4ce4d`

```dockerfile
```

-	Layers:
	-	`sha256:26be89f41d16c85e6d8a2311e93319645b0792a0e5fee2fd06f49c85e4c81fee`  
		Last Modified: Wed, 21 Aug 2024 01:05:55 GMT  
		Size: 109.9 KB (109919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8538160ef31bd11484a0c6229850b3539c5ecf429bb728139d3031499c01053f`  
		Last Modified: Wed, 21 Aug 2024 01:05:55 GMT  
		Size: 16.2 KB (16241 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:fa8c816860ec0536b838372c982d9230fb495231f457e576e5ccfabafaeca934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fe1c8487da6bc13f7260cc8021c7107a84adacc0ef2d951f02b72a87702ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57aead6d6c6a92877e32ff63a5bcbe8a741e037638fe7f786941a5df955e8b5`  
		Last Modified: Wed, 21 Aug 2024 01:06:06 GMT  
		Size: 3.0 MB (3003403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c89f26d142cad461af77ff13bace341b13393a1303507e4f4249292fa54291`  
		Last Modified: Wed, 21 Aug 2024 01:06:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6e54a27990d39afa88e65ef7360c13be573ef9955012ea900e152d9bf1b3c5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 KB (126410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2a865ec7f92328ad1abb23359fefa6f019fb0645a550dac601b2a04a3562e8b`

```dockerfile
```

-	Layers:
	-	`sha256:fe0e2c55c8c0e82b8aca691aaad639b56310c7785a427108c463232dbb03e2a7`  
		Last Modified: Wed, 21 Aug 2024 01:06:06 GMT  
		Size: 109.9 KB (109939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4aebfdcae0995b76b4beccea2f87ceb2d4788e33d545b5611c56534287e907a`  
		Last Modified: Wed, 21 Aug 2024 01:06:06 GMT  
		Size: 16.5 KB (16471 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:f94e9b5531f195e7ed08bc2ce42935b7370f079bc51918f0d4f2ea976b88e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6314336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516a4e56d6237900bc938fb6aa69bfb6414bbef5bf8df91d098a04e64fbc86c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d82dd844a6fa67bed9e46bf88c7fb1712a52c3b5a7d55f59a0ad08d90771e9`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.8 MB (2845929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57c397bc558aaea44ba15c76354ef0d9ef41bc30b40d9369841aff87e084aea`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5f099df76db8b39488afee78b90d533fd182338c4ecdd414b4a95af6d0197185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 KB (126000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1b4bf3c6ec662138a31d5dc08bc2752134ed43bc1e2062ade6a070eca27c50`

```dockerfile
```

-	Layers:
	-	`sha256:6dcfededda4be67ce759f8ae513299f1e40ba1b881d33fac1790985bc33af712`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 109.9 KB (109858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656c5a909c91a351f72e97b39d8593686e96c28da20557aed1e291f3d45e4f36`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:be6bbb423db3bd4ebaaf768db4401c201284848a97ee61ef6edbe07ab7e46324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6748243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63081b205d79ee8b8b121f9fede093b77badb0346697d8075ab940a573979028`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d968e9f2cea04056d50305530014153a349cc18ace32add7f230b5707db83b4`  
		Last Modified: Wed, 21 Aug 2024 01:06:34 GMT  
		Size: 3.2 MB (3176350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe62b7dd595d5a9ca12949296963606545d63916222bf9ead3dce1dc7ca594`  
		Last Modified: Wed, 21 Aug 2024 01:06:33 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:550da22ab39a1dbf8b5abe6986243b8dc72c794bc3050b327f6d79505e44fb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39974569b7f9adae6cfed5a01f7cdaf20caadeb16cf38186c7b261ac75071e44`

```dockerfile
```

-	Layers:
	-	`sha256:e85236c26044bc81cc6eeffd1d77e10a730c9afe3ca394c4578dd89bdf6e505c`  
		Last Modified: Wed, 21 Aug 2024 01:06:33 GMT  
		Size: 108.0 KB (107963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31030ece0620248aa1d9745ce8b25e04ebeabec7ce699da62573197d23bf48e7`  
		Last Modified: Wed, 21 Aug 2024 01:06:33 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:d156d2fefbd394cfa52b0d578df56ba25a183fedf786a91e47c4d6f8b5048b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc6cc32d1f5cc226c5e370c46afa7bb3fc4343bce02678a692e85d0d5fcb140`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ade14b464b94e0135cd43366861aca3e1642f8969c9a3fdaee7cd2e6e73d89`  
		Last Modified: Wed, 21 Aug 2024 01:13:09 GMT  
		Size: 2.9 MB (2854008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314776efadf44a96055b781d1df24514d6900c39d195f76d23f8026bc716cfcc`  
		Last Modified: Wed, 21 Aug 2024 01:13:08 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d923b4780f05d4c8d71c2306463fa504ada1731d7b681c1754574d12070a3481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 KB (124166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6d567103f5dcf27f5e7c40c419abf4a6d189d5d5f78890b71f677d6d3d2da1`

```dockerfile
```

-	Layers:
	-	`sha256:ff126533d5dcd64a0bfdea1bc3ed65073d2ba8f28ea47d13ffb904d80cc5433b`  
		Last Modified: Wed, 21 Aug 2024 01:13:09 GMT  
		Size: 108.0 KB (107959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:700b62c17a37f7446ad1aa49e093bfbaedc375a62461029ddee2b78bc2a2e341`  
		Last Modified: Wed, 21 Aug 2024 01:13:08 GMT  
		Size: 16.2 KB (16207 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:5908cf7a0c78f73697fa5313fea4361c30f67c1492a3eb75c59d609f0230b5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a9fddca325236d07631dc002696adb43ad79ddacd29fa195cbc75a0881d277`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_COMMIT=cf694865de527e597de5a906643a74037341a431
# Tue, 20 Aug 2024 04:18:22 GMT
ENV _BASH_VERSION=devel-20240815
# Tue, 20 Aug 2024 04:18:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Aug 2024 04:18:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Aug 2024 04:18:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cc26eb5afab46cc7c50ac8eece85f40a741ae173a6ee78002ad2eb568ca61f`  
		Last Modified: Wed, 21 Aug 2024 01:00:21 GMT  
		Size: 3.0 MB (3004264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c14da99e13a2d0844823f029d430fe700b9ee834c5441f54d7eaf429dd9d35c`  
		Last Modified: Wed, 21 Aug 2024 01:00:21 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e8d8b49adcb414dbe6522e2ac2e4632e5c66ba62ce839c2a2956202220ae2e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 KB (124100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f061f5350cf3b63cda28f365b8b067280a78c6c0cb671917619dbfd9365cbd09`

```dockerfile
```

-	Layers:
	-	`sha256:debb43bdd9c90986daa5e9af5996d15ff1383aacc024f65ef24cbbcd5d0b50e5`  
		Last Modified: Wed, 21 Aug 2024 01:00:21 GMT  
		Size: 107.9 KB (107929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc7d9007d1544573f92281b3ff1a3b4a8c258bd1e175330c50de2f8b26913234`  
		Last Modified: Wed, 21 Aug 2024 01:00:21 GMT  
		Size: 16.2 KB (16171 bytes)  
		MIME: application/vnd.in-toto+json
