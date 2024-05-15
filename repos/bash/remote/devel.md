## `bash:devel`

```console
$ docker pull bash@sha256:146d54a8132bae28020905961b60523d7746f33f5b13d572077244ad4bf1c669
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

### `bash:devel` - linux; amd64

```console
$ docker pull bash@sha256:4dd1821c9f1a619825fd658ef2e1134166781fb3fbb532b0a985e21f290d055a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6301116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe598cee02d799058ea8db5c7f561df287e04b0049992d6892da32d955f3f0fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9032a2bb1a73677beb3edab366203ffbc5d1fc21c7cd5807a0fa1a4aa893fcda`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 2.9 MB (2892055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c822f41afd67251659654dae451c33bdc68fcc5bb04cd3a6539f463809a63153`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:73c2880a39814d70cb932bd77d872b7d177bc0b1301212d542f74e65f085a070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 KB (126958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b9ebb08a1e23397314dfcaa13e563cf33441c9a275a9ae3cbcd9c74fd17f7b`

```dockerfile
```

-	Layers:
	-	`sha256:e2455f8b0c77345a543a8f22fe392422abf5531699468d132cdaba05f1aba99b`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 110.5 KB (110458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40a4aec2f56d1d1b8e7edee762abc5a3b2e9e0cb772d6714128dd54250f8e66`  
		Last Modified: Tue, 14 May 2024 21:57:48 GMT  
		Size: 16.5 KB (16500 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:b26e020a680da6ae182047fa18b849c6d0eaad6809fd98b274f76d299260e146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6008804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4199aeca6d1294815a725b0b3c2215faf160fd69432e2f200360dfe72a30f2b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12a1cd85c93b804e59a8b47fcff957bf603e4240366e6150692f566aec7652`  
		Last Modified: Tue, 14 May 2024 22:02:07 GMT  
		Size: 2.8 MB (2843075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b397aa128daeae30575bf5ecf931741d3570d8869c93902b818faf3941cdaf`  
		Last Modified: Tue, 14 May 2024 22:02:06 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:fce7a04e3ce8ea4dbc00cbb79986c5037df612e8a7db615a4c5da030e3b48c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 KB (16351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1be75df2bcec4b270b3b5e0ac426cc3853c8230205510abe6e56d2b01588413`

```dockerfile
```

-	Layers:
	-	`sha256:613b5570f2ee86e1dfa008a60be457bc7b8fc7c325aac56b39270aa6b277c8e3`  
		Last Modified: Tue, 14 May 2024 22:02:06 GMT  
		Size: 16.4 KB (16351 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:13cdfefb4551f40a64a9ae0484b116b2f10147b7b0db28a5f7e2c4e27e371408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5706300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06124d1280fe695ba438e3adf184dd4cd256466491708c72c4a768b59f9c4959`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dce5494d5b7d01c619a2e3772895237d5f08d8684b676a16f8ee4fc90c8abd9`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 2.8 MB (2787069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e14b1601786af4e4699135206cb28bc06d99e923fe68a36263eed66bf392efc`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b91c3e8700c8b0c85ba0547c3942e90c0326cacd0d2f3902b7d57f2f20918456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 KB (126698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f809398890e314c9318a6d9164f17b761b10ecfbb28e5d0cd5c891280b9a15e4`

```dockerfile
```

-	Layers:
	-	`sha256:0af5cc49310b1b8a2aeac190227a3ec0064d26834fe4b40e9022ae9b4816c66b`  
		Last Modified: Tue, 07 May 2024 22:52:11 GMT  
		Size: 110.5 KB (110494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1621166ba0dc017b8428179fd95bd3b4fee5ca1ca789517cfdfcf687a4be0447`  
		Last Modified: Tue, 07 May 2024 22:52:12 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:ad6398d314b91fe92e277937baf0015165828d3083530652f5871ccc21a74425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eeb6fe684238444b284d98153f1ad28a0db2a7c84996a5f70da8144a561d546`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02d3ec1322bd2c134ed0e25b6b37913ddf577de148bf998dae4a6497635e138`  
		Last Modified: Wed, 15 May 2024 00:29:31 GMT  
		Size: 3.0 MB (2994185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8844779f56c19a5b568f55d15f9df35dccf5ed9ea4e17caac4a12363ffcda492`  
		Last Modified: Wed, 15 May 2024 00:29:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d51639f83bd8c884eccf288e6c4f6d89df304136b1d1c73e233675967f6f91e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 KB (126813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e0beb784937aabbdd9c75aad3587a07964a7d2b4a69004b9e9b95d89fa59a7`

```dockerfile
```

-	Layers:
	-	`sha256:3aa4bce77f36beab0d7cf7c51c2adf19e5c2a3bdd78865838317602f2544575d`  
		Last Modified: Wed, 15 May 2024 00:29:31 GMT  
		Size: 110.5 KB (110469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d96464fd57b4d39c663912f3e2fd848bb3b367fe53d12f2f17e351d8bbcdd95d`  
		Last Modified: Wed, 15 May 2024 00:29:31 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:d50a770f2c8b1338062b02010c60179bc42dcb23837b4f56c62737888d17f38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6079039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c50b385d383b0fc278141fcfa7f79860401e50221c3ed90811603ecda951cb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050a8ae88d0380c139c902d002c87f1eb78d767d55cf735e68d10d85e835020`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 2.8 MB (2834616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce7910573c4bab0c8210bd42efd7614575b4ee40aecdc42758c24b8f1da85a0`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:211d6af4a10c961ab0507e00eed4a6c839be9f3c5cb7613994bb0d67f8db07fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 KB (126904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a9430a7c79ce8cbbe2531518dae838763f3bbfb565a223d9d217342b3a07fa`

```dockerfile
```

-	Layers:
	-	`sha256:a9b2d00e9ef6009a7372f280da23f0cfa08089853a7ec934e096ea466bf8dde5`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 110.4 KB (110433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b2a0770ea4d6cbf80823a6d0298af625079b422c39e0bca6c06724de9bcd72`  
		Last Modified: Tue, 14 May 2024 21:57:49 GMT  
		Size: 16.5 KB (16471 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:fb16468901234b2b45c13edb2d7a5ef3ab8bb497b2f5e10b21a4802e48a45fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6522680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a91e6fc105f7cfaf9089188016ea07df1e1d6754f451ef87fa3e6b945ac5f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_COMMIT=6fb61ee126cf5ffdcbff9ae51345838dc21d935e
# Tue, 07 May 2024 04:17:55 GMT
ENV _BASH_VERSION=devel-20240506
# Tue, 07 May 2024 04:17:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 May 2024 04:17:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 May 2024 04:17:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 May 2024 04:17:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd26f5b2cb8b657749020b7673d98786f88934f95e9b2f8f113132b35d2a1ea`  
		Last Modified: Tue, 07 May 2024 22:15:25 GMT  
		Size: 3.2 MB (3163987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec3bc802515906759e53fbfcbe2271c074504c170739a34a7f2244380714574`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ab50071d004a7b3d60b60043dfc324f1670e012824065484d63b4608078bf76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 KB (124710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12741f55f45791ebba59d1931262666415d2eef5a9767c36745a21ff29438ed`

```dockerfile
```

-	Layers:
	-	`sha256:752440ac51778d8c12a8defefc3e348394bfa7c08ca3b6b40a9b6e39f787846c`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 108.5 KB (108538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e20e6d6578ef3d883ec8e786ea027d261e454a25f680830566099acc8acbd60`  
		Last Modified: Tue, 07 May 2024 22:15:24 GMT  
		Size: 16.2 KB (16172 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:532a11cbef28e514c227239d2197124d90fe5a4dad4c2706e8d6681143f9e381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6236972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138aa5812bdebe9729a935960c86612c130a1de523c06379a2d1ffc235f53e2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_COMMIT=b3d8c8a4e7c5417d986f93f646ea740cb13c08d7
# Tue, 14 May 2024 04:18:09 GMT
ENV _BASH_VERSION=devel-20240513
# Tue, 14 May 2024 04:18:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		{ echo '#include <unistd.h>'; echo; cat /usr/src/bash/lib/sh/strscpy.c; } > /usr/src/bash/lib/sh/strscpy.c.new; 	mv /usr/src/bash/lib/sh/strscpy.c.new /usr/src/bash/lib/sh/strscpy.c; 		cd /usr/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 14 May 2024 04:18:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 May 2024 04:18:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 04:18:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bc51d567acb56d54857be0da944887b8e2f49018866057d05f372a0148db37`  
		Last Modified: Wed, 15 May 2024 01:05:50 GMT  
		Size: 3.0 MB (2994004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0c792e87ffd28de0feee00a4d3a21f45c28aef49eaf0ddf5e5a48acea38a6e`  
		Last Modified: Wed, 15 May 2024 01:05:50 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5b617aa2a3fc008b9d8fdba7edd97922d28a9129bd4e135b726a858ff69b66b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 KB (124838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa096993df659e33dcc5cd38d118eef1dda63c49a5cdd255c8ff8c2e26e78a31`

```dockerfile
```

-	Layers:
	-	`sha256:29f31d3af316bae25301b15ccc4cc5fc32900aa3c88c1c65aba99e71781ac2a3`  
		Last Modified: Wed, 15 May 2024 01:05:50 GMT  
		Size: 108.5 KB (108504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bbb4dcd40ff28b3710082cfd8181cd7e9ab8a6342575cd540a57e06b7ad312`  
		Last Modified: Wed, 15 May 2024 01:05:50 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
