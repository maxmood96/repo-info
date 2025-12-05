## `bash:devel-20251124-alpine3.23`

```console
$ docker pull bash@sha256:ad4a0ae97771999f43af5c8c85461ace964188e28a8114dad07455435c1f3506
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

### `bash:devel-20251124-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:2a8a50d8bf0ae4a68a3988ae1bb009e870acfaefd73b928d8bc8d38944d7dcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20247ae4367cecbf4ca8679f686fa20a17adb0bd3f9cb4d2bebf699f8c71e75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 20:00:16 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 20:00:16 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 20:00:16 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 20:00:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 20:00:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 20:00:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:00:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff4897bce083edf00423219d3500e97ba307608f66067cff3de6c4a09381772`  
		Last Modified: Thu, 04 Dec 2025 20:01:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d92dfa3a99ac0d498d2dbcaede2c7dc38ee6fe94070955ba64e5b5e79f2ae3e`  
		Last Modified: Thu, 04 Dec 2025 20:01:06 GMT  
		Size: 3.0 MB (3003370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e08103f162a9bea4e41f5dd46084504b1a4b7406640ce21e300cc4581999166`  
		Last Modified: Thu, 04 Dec 2025 20:01:06 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f57aebc30a16663b49bed4bf49fed8c364fba6d25641b0dc4b3ce422c829f50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9f6d268163b0c93afdfc2096a792fe27c9d9f727f69cbe96c3b547a4ee2b04`

```dockerfile
```

-	Layers:
	-	`sha256:5d2a15c2ff650b3540f4a9c07d0f14eb4de36bf9cafeddf84e2b8a51c4c65250`  
		Last Modified: Thu, 04 Dec 2025 22:03:09 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacb3e95271ae73ed0ea5264aba6f5c18745d6182f09ebbf79bcb3508632dd88`  
		Last Modified: Thu, 04 Dec 2025 22:03:09 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:662c5d410c7b4ac35dd5eaf26e1100f68a8dd100581e1f7af92f42aaf91a3881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6533152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcb28a04e653687691f443881887bda60f7ab93d924c60ac44100307d2083021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:50:25 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 19:50:25 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 19:50:25 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 19:51:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 19:51:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:51:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:51:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4d33204d0548bb541ba61c7e4085ef2934485280e75f97cb1ae577ccaa3de3`  
		Last Modified: Thu, 04 Dec 2025 19:51:23 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3369a44b13d3e3516f9bad84a8313f0cc7fe6c6390fa96ded83e3169cc7d45`  
		Last Modified: Thu, 04 Dec 2025 19:51:23 GMT  
		Size: 3.0 MB (2964466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a765045946c03447da1d437e1c9c84f77a4fbaced4b3cd29a227dc685d30055d`  
		Last Modified: Thu, 04 Dec 2025 19:51:22 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:d25e30bcf21eb6afc134698f2fc8cd513d6057ea89c4a3bffffd4cbe34ede7f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5c4344b91c3fc8ea42b286f656f1ebd20d39b87b2b21d787029267a5c8e311`

```dockerfile
```

-	Layers:
	-	`sha256:3a30d1d2398e5aaa90206260dcb6a99d3548c51389a13ce9d8a31baade1929e3`  
		Last Modified: Thu, 04 Dec 2025 22:03:12 GMT  
		Size: 17.9 KB (17909 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:3b094ef611de3baa9675d301de46a19bacdbb4087587f5fdd248cdabc55ccfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6193571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b444455679d8470887e1101214b2cb0056961ecb3acf5ca0e063024454c03f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:49:10 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 19:49:10 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 19:49:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 19:49:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 19:49:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:49:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:49:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1372ea475d57a01c3ca0be1c6b291cf4e87c13e8cd884c6cdda5f9e1a5692718`  
		Last Modified: Thu, 04 Dec 2025 19:50:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd9dc8bee463a5b1c545a172faace094b6dc891480b97b039ce1e2b111d29ad`  
		Last Modified: Thu, 04 Dec 2025 19:50:08 GMT  
		Size: 2.9 MB (2914318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1561a03d6a89e09bfa0cf1e86c4809e45e014aee55aa8cf53543ce10774f9f`  
		Last Modified: Thu, 04 Dec 2025 19:50:08 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:4fdb1d45fa7790997d8b0687fc93f653f4932412be13642844cc5180b9df9ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c854abf78f4866c3f4945bc5c8831ca242650c0c1a46c320105d274612e0e862`

```dockerfile
```

-	Layers:
	-	`sha256:aca174873d0fe7c5cbec70e816f5aff11bbef274a60918a3f922d2ae2fbcb51a`  
		Last Modified: Thu, 04 Dec 2025 22:03:15 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb409dab5ab916ab4fce26eab616f3d8c8545d665b078adae4ca6632c752f849`  
		Last Modified: Thu, 04 Dec 2025 22:03:16 GMT  
		Size: 18.1 KB (18124 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:908afd43809feb626be4194628bf3b4e4afb882b919ab8b696a855d3acd4ff37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7268673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf2c93a899a9cd2be800f4bf4b2dbb6d6ee465ead0d78b5048b6e9402fc923e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:56:10 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 19:56:10 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 19:56:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 19:56:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 19:56:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:56:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cea10bf829ed0d9ec9307951bd90f7bb42852009fe42fa93348d075d9228df`  
		Last Modified: Thu, 04 Dec 2025 19:57:00 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2253ec21c1a49166f9d6892c63caad3c641d522e8023b0a3dcf05ce549f5ff2f`  
		Last Modified: Thu, 04 Dec 2025 19:57:00 GMT  
		Size: 3.1 MB (3072683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2ca4c818e4c8cd0bbd2f04949790c1db843aad20e2dd6ad99facf554affd8`  
		Last Modified: Thu, 04 Dec 2025 19:57:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:ef3e6dbbd3a1d3f5865f8a37ad4e7e6fc1cbc575a7fa348582606b04ef8442cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e466eb3095301c5d30fae2fb7c5ce1da62290e595654985fec1284ebbbdfd92a`

```dockerfile
```

-	Layers:
	-	`sha256:bc39b6e2a4ff8020849943706440cdbac637485501ba34f22232002e59c923c5`  
		Last Modified: Thu, 04 Dec 2025 22:03:19 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a75a04b7a4bd01011a8825beb2de90e3345921f785da0e4d6babbfa5a3590ba`  
		Last Modified: Thu, 04 Dec 2025 22:03:20 GMT  
		Size: 18.1 KB (18148 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:b6739a0b6bbe89d88352a84a261c14d79bcbe6c9e91fcf4bec70db7be519bde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6618466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac71c5aecf8d8745820cf3238ab2728af0f11991e1388912ce28dffcaed932b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:48:35 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 19:48:35 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 19:48:35 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 19:49:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 19:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:49:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73249ae29d3f38f1fa6eaac9b51ad8f96d68508ef0a2608f5c9c7495fdd6abc9`  
		Last Modified: Thu, 04 Dec 2025 19:49:30 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7611c440e93879c9ddb41555ee49804ce9860f2f4661d651e6247efa165fee5b`  
		Last Modified: Thu, 04 Dec 2025 19:49:30 GMT  
		Size: 2.9 MB (2931824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9a04dc9c467cabb5956b8486f3f08ae178452e2af50b218e9a476e5bdfb7b6`  
		Last Modified: Thu, 04 Dec 2025 19:49:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:fe71ec1207435417178cd2355fa52250ab13c981f8fe467a1093cc9d8695cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754307ed0d37c70138ab991377ab96724e2f03304a42442243b59b8282c700fa`

```dockerfile
```

-	Layers:
	-	`sha256:56ff8f9c21f647f3b268838c6565d0601b22cacf2d0f8e8f76704efd175a6534`  
		Last Modified: Thu, 04 Dec 2025 22:03:23 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc62fde5ad3c7774dd68baf80dbd463c618a5eee2eed15a863f925cf5021ab2d`  
		Last Modified: Thu, 04 Dec 2025 22:03:24 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:716d6bb8759b4afe4c405219e6f17b0816eb477a8e7d915ab21ea11e532dfc41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7136339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99ed03acbffe11fb7e8b9eb92586107c73363521d480e59fb98ec9e197bed71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 20:03:40 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 20:03:40 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 20:03:40 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 20:04:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 20:04:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 20:04:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 20:04:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163caba452ff1e8782a3a9a4f4ab761893151086d3dd0e86104fb8207bcec9e7`  
		Last Modified: Thu, 04 Dec 2025 20:04:56 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a71104a2048c2c686c971ec1ee4688cb5adeee17898eefe4ad2d504503af7dc`  
		Last Modified: Thu, 04 Dec 2025 20:04:57 GMT  
		Size: 3.3 MB (3308529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9334088398706ee9ce1b1f063fe9df8d452085d1560b333b51c66e9e02477f`  
		Last Modified: Thu, 04 Dec 2025 20:04:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:1e8e6be55d7a10ab589185912385e0695f29b45cd9d2ce2d873e87ad58bb38b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c59e2d7e5d24623909e65dc88ebb247f06ad41e9d5f02fda41301e86c35b0d3`

```dockerfile
```

-	Layers:
	-	`sha256:a303f36403b4bc3372232369d52a9b27d00a0a1d3275aedb7b22a22a77f9c8e4`  
		Last Modified: Thu, 04 Dec 2025 22:03:26 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:694df4d5ac63212c8a187c8af4945cf02f89bba660fe1187733a45ecbf8048ad`  
		Last Modified: Thu, 04 Dec 2025 22:03:27 GMT  
		Size: 18.1 KB (18088 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251124-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:4070c8eca52953a04936a04d036f180fe186fd6565b30dc9ed1b4f644bdc446f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6818268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf9b9ffcbf7a549ac08b34b884756b65d648eb55a0cf35f62975994c13be50b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 19:52:16 GMT
ENV _BASH_COMMIT=4e705ed53ac364ee110f0b2fbeeab9d3301fcb6b
# Thu, 04 Dec 2025 19:52:16 GMT
ENV _BASH_VERSION=devel-20251124
# Thu, 04 Dec 2025 19:52:16 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Thu, 04 Dec 2025 19:53:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Thu, 04 Dec 2025 19:53:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 04 Dec 2025 19:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Dec 2025 19:53:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0560e82e9a688814566c18de0a83ae105face12043880cdf887b45411f28c6f4`  
		Last Modified: Thu, 04 Dec 2025 19:53:35 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d50ebb3a842b66c2e7e0f5a18a87735d805b8bfb9477937038df87fb8baa57`  
		Last Modified: Thu, 04 Dec 2025 19:53:36 GMT  
		Size: 3.1 MB (3093665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76d4597157755f0196ebde6592a44cbd2b5f6749ee2b66ef74c57119aafb665`  
		Last Modified: Thu, 04 Dec 2025 19:53:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251124-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:50e3b49f7d4d60c0211b48b9bb9a7943a775fde0c148238d021fec3484edbfaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0f759e7c498915c0a9ba6069991efc2c25d422383bc6355251e183688f99b0`

```dockerfile
```

-	Layers:
	-	`sha256:e546c85bc5547bb3aed848111cdb360c2d15222102cab08067d5249a09aed74d`  
		Last Modified: Thu, 04 Dec 2025 22:03:30 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b46b7371edbb1acc2a5a6042f1c9e08989793c5a0c6e3cc5d94fc58f55db75`  
		Last Modified: Thu, 04 Dec 2025 22:03:31 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
