## `bash:devel-20251217-alpine3.23`

```console
$ docker pull bash@sha256:f2786368d457f28437210dba78845707307014f86823dee922c89ef8a9b1d1b5
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

### `bash:devel-20251217-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:adea67d16d984eccdbd83d7ffb120d9979075df4bee2a68a0570c2157aa724cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6868043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e9679524473d4e9cd46d77549edfd8bc085c68b76c9f978355e42857692020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:18:15 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:18:15 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:18:15 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:18:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3995fecb1fe4070195f3116c32da5e9e19d13dd2c4cdd6e2668e76b7a1eb3f`  
		Last Modified: Wed, 24 Dec 2025 05:19:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7722e4c72b2fe9f628b1b316a9544364a805fa438f5af1eb8b6c3ed1ecc6770`  
		Last Modified: Wed, 24 Dec 2025 05:19:07 GMT  
		Size: 3.0 MB (3007146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552fcf6a173271ce64e86b95318d2a76b279958aac029943ec4cbfb1c845ab07`  
		Last Modified: Wed, 24 Dec 2025 05:19:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:8a6ed005a244d17f77f891186df69010a3d95ad59985a8d24044e1b04bd0964f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 KB (135478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b224c3187ab69f3388208c3d15d851fc51d8e12bf7bcf2f50cbfd6c72ea684c`

```dockerfile
```

-	Layers:
	-	`sha256:f7b2eca15ee59254068d107f8e3e38e42303c734020d82bcc4a740f0ff6407fc`  
		Last Modified: Wed, 24 Dec 2025 07:02:52 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d3c4a95adc4babf825129bd6841c778a4b5318a7e4d22207227cb13f711881`  
		Last Modified: Wed, 24 Dec 2025 07:02:52 GMT  
		Size: 18.4 KB (18356 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:e629a8275c886e906e4f8b3ce651dd2881f2cf5b1827dec2c5cc6aeb2f896d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6537970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f508292701e716e9473ced8f6b0dc1601ce886c8caa2f97219993e400c6b9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:13:37 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:13:37 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:13:37 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:14:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:14:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:14:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1016078b37f2a3e880042f45cf82c8e486645b83333723c53b424f32daed372`  
		Last Modified: Wed, 24 Dec 2025 05:14:31 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023e9d4ca6686d30aa62e54079822936e8e2d836bb2a459ba080cf4d094415e`  
		Last Modified: Wed, 24 Dec 2025 05:14:32 GMT  
		Size: 3.0 MB (2968747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a090dc93f7a9e3f13c28e21217ce7850ea181e4c1ad6642aa40fe7232c3c1c78`  
		Last Modified: Wed, 24 Dec 2025 05:14:31 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:3e9c5b06b3e0b2d6aa09cf0a86c803640cf08c739d718f00dfea0264ba3d8f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db1952aa87e014dacb21e3b809b9c598e1f689e1591781c4e33d52b72323609`

```dockerfile
```

-	Layers:
	-	`sha256:ac270e84bf3b366dc05805d8ee18d54e8a8cb2bd6eb03ca6d4be564cc6a48157`  
		Last Modified: Wed, 24 Dec 2025 07:02:55 GMT  
		Size: 18.2 KB (18221 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:ae8fbdf4267217e7eed2d44ee541e18183aac6defe33098bc667dcf90792a9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6198519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50faacefd203a1be39f5a95d8144980f5677f767aef6b792e86b97852e869d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:12:55 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:12:55 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:12:55 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:13:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:13:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:13:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:13:37 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54448af60638e75a6776e4cfa3a14331ec279c5cac7a182fc75a8814d9c7dca3`  
		Last Modified: Wed, 24 Dec 2025 05:13:53 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ff0494db9dd1283272ff1d2993755147f9ab9b69a90f7bb256d5d4375d1090`  
		Last Modified: Wed, 24 Dec 2025 05:13:53 GMT  
		Size: 2.9 MB (2918343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f250efafa4bfa01d9f9f1d12936f9241aa5ee101bf14a2ec3465b9913aad1d62`  
		Last Modified: Wed, 24 Dec 2025 05:13:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f9426c771fe7114ac895fd569e6ea946e59a7e43fc33aaf53ea27300e8dee249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748666ba51bceef3631124cd05e16d5e7df4ff8712d4f41d6385aafd0b2e849d`

```dockerfile
```

-	Layers:
	-	`sha256:83c9883d4be0dccd8d7d5d35c8e5c0fc57ef37583b1f743360ee155ca224b52c`  
		Last Modified: Wed, 24 Dec 2025 07:02:58 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9ec758eed919e5923a23ccd112c7242c8e7d56ab8203612c233ad6004eb6050`  
		Last Modified: Wed, 24 Dec 2025 07:02:59 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:8ac266c140681c5cfdf844c96abdec584c27457e11ca3de25eae62dd28284330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c8c82dc13c7e05ebced5355955b16a4ceb7a417e9d443f59e8931e5b9910c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:18:23 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:18:23 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:18:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:19:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:19:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:19:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:19:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c209b4d7f35c40673a74bbb71b635cf23b0e13dc927784addd02fd13344222`  
		Last Modified: Wed, 24 Dec 2025 05:19:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1db3e373128e2ab5a1283cbb564b6d3f170f4483574e16be9891a1bd7e4198`  
		Last Modified: Wed, 24 Dec 2025 05:19:13 GMT  
		Size: 3.1 MB (3076347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7de9c387a94cf9451c149a5971866dd1c4678697444bf052adb1722cdb0045`  
		Last Modified: Wed, 24 Dec 2025 05:19:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:7e2a6042ee5407887f1a75dc12292b4f9ca764a4413de34d50327bc1a0f42c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (134988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74b664bbc7c0a3a6ca813cc2246bf65d303afc943ba740829321c536b360941`

```dockerfile
```

-	Layers:
	-	`sha256:47d974399b3b7a971d02e09e264dc9bbbb911fbc6c31388a41b4a06ed10e9f14`  
		Last Modified: Wed, 24 Dec 2025 07:03:02 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e320f5f656bf50f6f6647e6a1201f79eee3e7ccce6e100ba8d0a7c3b6ad206`  
		Last Modified: Wed, 24 Dec 2025 07:03:03 GMT  
		Size: 18.5 KB (18460 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:8b31befc3c988d98d87313f2e071a6ccb6fe16e2151c0d8eeb397bef25e6d136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8753d771d014f355dd6e54d63131a36f855e30a382b6724d7a134bdaf2d5be19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:13:09 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:13:09 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:13:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:13:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:13:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:13:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:13:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9957cb172638136bd8356e13a20f1f3d9f60e604e7e15845a074b01a26c284ea`  
		Last Modified: Wed, 24 Dec 2025 05:14:05 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f542a3f8f7f7555bcd99bd94a52ffed684a711fa83db3d8b9e7b44b0f0bfdf0`  
		Last Modified: Wed, 24 Dec 2025 05:14:05 GMT  
		Size: 2.9 MB (2937528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364df449f44db5be4f4fb948bc2ab214b7bde09ea1a731f1d1c019d7d0a6a9f2`  
		Last Modified: Wed, 24 Dec 2025 05:14:05 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f7b6c3cb4d916c3a1e0267a49561a29760e770ede33b0e5a15163cdf833239a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 KB (135421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95b2550c5e0ef87076f84e17d83cc3657dc8f3eab8f021230f87a0c5f021f0c`

```dockerfile
```

-	Layers:
	-	`sha256:8631493fdeb008a12bea35f6588f1b1f7137bf43fcd3086a90ca98851adc908e`  
		Last Modified: Wed, 24 Dec 2025 07:03:06 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c31fab1fab7764a542c44b4695cdbdd9a6bb22154b82eff8e0bedd5455ffcd6f`  
		Last Modified: Wed, 24 Dec 2025 07:03:07 GMT  
		Size: 18.3 KB (18324 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:58f6ff92195e331f764dad816fc7891d77a4e733335633ae66b30a2d0b9d33e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cb517c4191078e3afae134013c6a79c1cb3569a0d192dc2424f70a283820e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:25:58 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Thu, 18 Dec 2025 00:25:58 GMT
ENV _BASH_VERSION=devel-20251217
# Thu, 18 Dec 2025 00:25:58 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:26:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:26:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf056449837c26e20456ec1de3d317628e37795775a4fe3956dc4871707fcd71`  
		Last Modified: Thu, 18 Dec 2025 00:27:20 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d919816b4dd26a2739686680b7a0dceb2b6b8742e1faa3bca3d144c60da02d`  
		Last Modified: Wed, 24 Dec 2025 05:26:48 GMT  
		Size: 3.3 MB (3312238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a000284ad092c0515f632fea0f27014e30514142816d67f4696c5c16542122b6`  
		Last Modified: Wed, 24 Dec 2025 05:26:47 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:b2082d69e72ec1960f217dab80b9821be74f02417653621854ae92f0a5779367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8864ef800050133f27383a39697546ab6aa488f999a16a5055eed02b84243f`

```dockerfile
```

-	Layers:
	-	`sha256:aef037613beeb4db6201b139ca4427b722ec273306a122e9c57f5c493bf95624`  
		Last Modified: Wed, 24 Dec 2025 07:03:10 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf755568f24c40c31003c4cebda6af0f23148532ee9c1fa33b0490e7815caaa4`  
		Last Modified: Wed, 24 Dec 2025 07:03:11 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:123a1f9ccefc7eed6b6f7a6d6c2239104fe76318fb524684897988bcc5bfe229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd60c7b6480d1eb07e9abf4eade76eb5d8f78538b9a07e8146ee0d7256d402f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:12:39 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:12:39 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:12:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:21:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:21:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:21:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:21:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4513d4113afefc12d5002e33ef2b29b54dd17341532e87f1b9aba2c3f330253d`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae171dce9b160bd5279a6952dc648c2472e7b2c31b54e65e82999a4a149f148`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 3.2 MB (3199614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b75468e889e284723c6b215903b57bc4b1a67ddc97f2c39c44eefb9b308355a`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:33cf92395a71be328f2805d02e09007f3d6eef48857f8261a7c0dc7e82dc0185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e87687f59b81ec17fd75d118ee59e872b3eba1d5ecacf7c0e6d65bbcacb3009`

```dockerfile
```

-	Layers:
	-	`sha256:21620b5e1bdba187d1d04c7e8264c8a8332c86e0b0fca85571f9f3e87cd16f17`  
		Last Modified: Wed, 24 Dec 2025 07:03:14 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e7cd3acb270bf18180eef5762e8c7aabde33e3c0c1ba4c263ed2cd76e082c4`  
		Last Modified: Wed, 24 Dec 2025 07:03:15 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20251217-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:85fb83d36f5ee647c7bdf36946e6c252e95c3863427fbea4d3ba3c076652e6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6822865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3477b2a1a794bab1f632496b6a0e6879fd7229f98694aa80f991250dba02e2ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:26:06 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Thu, 18 Dec 2025 00:26:06 GMT
ENV _BASH_VERSION=devel-20251217
# Thu, 18 Dec 2025 00:26:06 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:12:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:12:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:12:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:12:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74850a391a16eeee8ef302a64bd78c66b478afe49d8a2b62f922f56037b9d4dd`  
		Last Modified: Thu, 18 Dec 2025 00:27:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a7bd2c53ddc8450822b5e03eccd8afccce5b1301db41d138f9997d646b4ffb`  
		Last Modified: Wed, 24 Dec 2025 05:13:21 GMT  
		Size: 3.1 MB (3097764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e61a7b2bcf787f405901aa4875e11ba71ce85a9160dac9af3a8e71a5e84929`  
		Last Modified: Wed, 24 Dec 2025 05:13:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20251217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:60f8f8ac4650a1e1d637f6904bd9a332bbb3e39f1d05ddc840f19a49038d8a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244ec2a96eecd2a08207fb990235acd10e3a63fa50487e1c32233c4c57db57e9`

```dockerfile
```

-	Layers:
	-	`sha256:e2a1a63b4f316a4c6b4b630ee18a8efe85ae80d8472d1fb6d95a2d8ce97065d8`  
		Last Modified: Wed, 24 Dec 2025 07:03:18 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d806dd437f583fd172b596270cf0fd0f677a560879cc466367a4c887f326f98`  
		Last Modified: Wed, 24 Dec 2025 07:03:20 GMT  
		Size: 18.4 KB (18355 bytes)  
		MIME: application/vnd.in-toto+json
