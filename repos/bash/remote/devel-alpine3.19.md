## `bash:devel-alpine3.19`

```console
$ docker pull bash@sha256:78b4fe3bd0d10da27055513918b22f2d302679e042525bb17eb4c8f58d18ce34
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
$ docker pull bash@sha256:4a83f1c504866b2623ad2ba04159b070f3f192245e0485a135f9948ec01ccbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6268553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85442231cf36581ee2db2290f53f1f6f518a36a1505f79afe09f66be81397efb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f492a6ad2e22443027695b34548d28b27237fadf2564dcdc3aefe198b0c999`  
		Last Modified: Tue, 06 Feb 2024 20:52:16 GMT  
		Size: 2.9 MB (2859492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153ecc4f92473bfaa003e39bf341df6842d838c5844bdf371633ad24c9bf19b`  
		Last Modified: Tue, 06 Feb 2024 20:52:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:f0698ae97640fd65cfe93761be92d54518f23e399566a64be6cdddd8a45c3b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 KB (114074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269ceacb828684dc50de56ec2062e17dcfab57c01c825a424e5fa9fecd1c67c3`

```dockerfile
```

-	Layers:
	-	`sha256:5f599adf7faeceb4b3fdb614be1db495695a90d1bf9815d4447e46d6171c1d4f`  
		Last Modified: Tue, 06 Feb 2024 20:52:16 GMT  
		Size: 97.7 KB (97738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29152589a0b404c4d99d9cbb5d5feaef9750e0cd0645ea4d9b987ba677c511e1`  
		Last Modified: Tue, 06 Feb 2024 20:52:16 GMT  
		Size: 16.3 KB (16336 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v6

```console
$ docker pull bash@sha256:f8e5819978971b2096cbc1afcb44a6778cc67645a19d53b3475dede9a5e9df74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5979558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e105e18675f4105267ff124f882aa9e46e24f88f8aae8cb732784674da5abe46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed40667b499d307edb9b4a1adccc29d79f5e0b9d2360c784268b1a4d48345200`  
		Last Modified: Tue, 06 Feb 2024 23:34:16 GMT  
		Size: 2.8 MB (2813825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef466772a0c4f73147bd42ff4d9b4d1eae7ffafe86a4390a68929aa117c645`  
		Last Modified: Tue, 06 Feb 2024 23:34:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:6c8beebb4bc6d347ffbde6ce3fb53776a0fc22858e097e7c0aaf23f426e18bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a80981ef1efa303379f483885dd42947f1ad461b7a0d59ebe3d608fae1e362`

```dockerfile
```

-	Layers:
	-	`sha256:309ce5ede84afe1a87699ae8d17b4c80da1ac549219d7d164f76e6a3abf72033`  
		Last Modified: Tue, 06 Feb 2024 23:34:16 GMT  
		Size: 16.2 KB (16190 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm variant v7

```console
$ docker pull bash@sha256:1662c5a52a4b6a409e1056fdafee924e56505f02deec6115e25dc6bc78c40ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5681997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5071499aff3b8db2fadfa4448879477dbb918e8edae2b125dc2db9e0e094bbd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39332213a9c9ff5e55f3b1dd79e467b712301f8aad7b6a5381ff3bd18958f0`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 2.8 MB (2762761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958384b65facfc72616cfd2de95db2b8f39f479a72cc6e30e92f3f963cd05a02`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0d8eb4faacf8c4cbac9ec506d9f37249d68508376e5a961c8ca29b8b87554dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7323eee9659c83f03fa786e31a25b1b81b518a9d760b243e880b99689a72af3`

```dockerfile
```

-	Layers:
	-	`sha256:0528a1914ce2c7c06ae34b3da240edb72b889cd04c331d27e3796f855d71cd63`  
		Last Modified: Tue, 06 Feb 2024 21:15:43 GMT  
		Size: 97.8 KB (97774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901aa743294bd7e455314a2a4bc43416a2c74193e91b09c4697547db27e4a1a8`  
		Last Modified: Tue, 06 Feb 2024 21:15:44 GMT  
		Size: 16.2 KB (16240 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b29cfc871ea5139d3fc5cb0957dc1a84fa0441f424a9f345323d69081128a34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6312952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7069cdfe774726db54b8c329ae1b79631a05b5b1104edbd532238f9274219f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd94aa6ba7731b818e533048dc96426fa7e41dd6d35bb651e485e1fa471ab28`  
		Last Modified: Tue, 06 Feb 2024 21:32:56 GMT  
		Size: 3.0 MB (2964900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dc9906522430cd8595c7b38dd209679ce764504b05535ff764f816eb0d1c50`  
		Last Modified: Tue, 06 Feb 2024 21:32:55 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0569e7261db85e52619ce7818dfb80ac81e489b5694e48ea7f08ecae4e076345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 KB (113929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e2a1067c29efd1fa14d8ca052cba427b5fdc8dfcdc057abc867abf912cb85f`

```dockerfile
```

-	Layers:
	-	`sha256:2f9c9427212ce3367d35c833dbbfca90c3c115fd15147065d08e05c2592f9d4a`  
		Last Modified: Tue, 06 Feb 2024 21:32:55 GMT  
		Size: 97.7 KB (97749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6774eb4dd2c3bb0aa0320feb68e14e1d0957e25848d494d5e1b2dd02f7b864a`  
		Last Modified: Tue, 06 Feb 2024 21:32:56 GMT  
		Size: 16.2 KB (16180 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; 386

```console
$ docker pull bash@sha256:106d44f20fab5a6a137287e024a3634c676d95f7e775d51f83d17a387c97b683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6052059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deaea5065d9c35199ed5582ba3a56010e961bdf0390b9f4ac5538f0769ad9f3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c74c168fe970d864f136115d0d7444a15005286b2f4e0abbe62a5f51f30bb2`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 2.8 MB (2807640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e87e1da61672f1558758ad618347805f4d429fc9b4ffecef717997b13e8b156`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:717f864553b7edbb153ae1895a2ce7dc63bf9a9faa68790cb7fb0b91b984a066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.0 KB (114020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f89ed899a03284c65a418d691a18f3865c8af756d5382a50845c2f377601d25`

```dockerfile
```

-	Layers:
	-	`sha256:f9497b998df074fe61b87d932f996661e5858af78923361fffa0a61822a31278`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 97.7 KB (97713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e18368389c39de100deb12f90b6fcd2530de8423fb2bb541649ea1c31bbc79`  
		Last Modified: Tue, 06 Feb 2024 20:52:18 GMT  
		Size: 16.3 KB (16307 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; ppc64le

```console
$ docker pull bash@sha256:5bbde3d14aebe57e0dfe2b0b4999948028799b0da82261c9d01a978fc2f24ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6493771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f974873a521c98b11efb6c6c8d77d54c9a6f38f7dafb1054673dc66b2b6cf4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dac185e9baa17ae736bedc73bd1e314be8991800eb2489a37c7a07468e1daf`  
		Last Modified: Tue, 06 Feb 2024 21:14:08 GMT  
		Size: 3.1 MB (3135082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8228b0860bdec7a5182a635f7663fb05b4e3bfa6880d6d292c285f78fc149efb`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:0d150750716c8c1f3134922c14cd58faa7dffd65a71cb276b59d06c1e543c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a04f8396478b2428d9ada38a1dd27a042c5557b7bf71daac5de84a08fae4ec`

```dockerfile
```

-	Layers:
	-	`sha256:6016a0fe176f6b8ed4f6102dc8447b8f5e04aefefb8ee42cb9767e5a981dbde1`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 96.1 KB (96136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df60a4324a9ac4b639424c7c404f508b93d4b525b52d580b741646ad620cf57`  
		Last Modified: Tue, 06 Feb 2024 21:14:07 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.19` - linux; s390x

```console
$ docker pull bash@sha256:187f2a7cbdb3c4854beb5ac917d8c11eb6857d8071a3b80d66c5649421676b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370e33b802232f971179c679457feed58a3d263ad3e47c0ff9397f1ea5a248ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_COMMIT=35465406cdae9cd4a15e7f6699e657b5d09bf7bd
# Tue, 06 Feb 2024 05:18:03 GMT
ENV _BASH_VERSION=devel-20240202
# Tue, 06 Feb 2024 05:18:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Feb 2024 05:18:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2024 05:18:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08645f5ad5e1a8b3e99c138f2e849d2009892158f5a30980ccac253c4866727f`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 3.0 MB (2961454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b82ff5658f91ac798685312b3a5282702af2366675b25f0f245b2a14abc8d`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.19` - unknown; unknown

```console
$ docker pull bash@sha256:64dbaa95de77160f3590ab8aff4f61416aa89c5dfcaf820e22ec411719689c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 KB (112271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0940a9f384d7eb33ea77146ee5a6f2b7201886d23d0c12514dadfe952d4dfb`

```dockerfile
```

-	Layers:
	-	`sha256:4425672f0629b9c5d4dfa0e1980c25aba71059f008747c8af9a963adc6a9ad46`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 96.1 KB (96102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438c766799eeea5d764dbb5057b2d75cf12633b4c44c574924796286df68362f`  
		Last Modified: Thu, 08 Feb 2024 00:34:36 GMT  
		Size: 16.2 KB (16169 bytes)  
		MIME: application/vnd.in-toto+json
